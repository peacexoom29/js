# js
// Get references to the Send button and message input field
const sendMessageButton = document.getElementById('sendMessageButton');
const messageInput = document.getElementById('messageInput');
const messageArea = document.getElementById('messageArea');

// Add a click event listener to the Send button
sendMessageButton.addEventListener('click', () => {
    // Get the text from the message input field
    const messageText = messageInput.value;

    if (messageText.trim() !== '') {
        // Create a new message element
        const messageElement = document.createElement('div');
        messageElement.classList.add('user-message'); // You can define this class in your CSS
        messageElement.textContent = messageText;

        // Append the message element to the message area
        messageArea.appendChild(messageElement);

        // Clear the input field
        messageInput.value = '';
    }
});
// Get a reference to the New Chat button
const newChatButton = document.getElementById('newChatButton');
const chatList = document.getElementById('chatList');

// Add a click event listener to the New Chat button
newChatButton.addEventListener('click', () => {
    // Create a new chat item element
    const chatItemElement = document.createElement('div');
    chatItemElement.classList.add('chat-item'); // You can define this class in your CSS
    chatItemElement.textContent = 'New Chat'; // Set the chat item's text

    // Append the new chat item element to the chat list
    chatList.appendChild(chatItemElement);
});
