- [Day 12](#day-12)
	 

# Emoji's Search Application

- Building an emoji search application in vanilla JavaScript using the Fetch API to retrieve the emoji data.

HTML Code:
  
```
<div>
  <input type="text" id="search-input" placeholder="Search for an emoji">
  <div id="emoji-container"></div>
  </div>
```

JavaScript Code: 

```
const emojiContainer = document.getElementById('emoji-container');
const searchInput = document.getElementById('search-input');

// Function to fetch the emoji data
async function fetchEmojis() {
  const response = await fetch('https://api.github.com/emojis');
  const emojis = await response.json();
  return emojis;
}

// Function to filter the emoji data based on the search query
function filterEmojis(emojis, query) {
  return Object.entries(emojis)
    .filter(([name]) => name.includes(query))
    .map(([name, url]) => ({ name: name, url: url }));
}

// Function to render the filtered emoji data
function renderEmojis(emojis) {
  emojiContainer.innerHTML = '';
  emojis.forEach(({ name, url }) => {
    const emoji = document.createElement('div');
    emoji.innerHTML = `<span>${name}</span><img src="${url}" alt="${name}">`;
    emojiContainer.appendChild(emoji);
  });
}

// Event listener for the search input
searchInput.addEventListener('input', async (event) => {
  const query = event.target.value.toLowerCase();
  const emojis = await fetchEmojis();
  const filteredEmojis = filterEmojis(emojis, query);
  renderEmojis(filteredEmojis);
});

// Initial render of all emojis
(async () => {
  const emojis = await fetchEmojis();
  const filteredEmojis = filterEmojis(emojis, '');
  renderEmojis(filteredEmojis);
})();
```

In this example, we use the fetch() method to retrieve the emoji data from the GitHub API. We then filter the emoji data based on the search query entered by the user and render the filtered data in the emoji container. The async/await syntax is used to handle the asynchronous nature of the fetch() method. The Object.entries() method is used to convert the object of emoji URLs returned by the API into an array of [name, url] pairs that can be filtered and mapped.
