# API Integration Challenge

Welcome to the API Integration Challenge! This is a practical coding exercise designed to test your ability to work with APIs, manipulate the DOM, and handle asynchronous JavaScript operations.

## 🎯 Objective

Your task is to integrate a real API into the provided HTML interface and display the fetched data in a user-friendly format.

## 📋 Assignment Details

### What You Need to Do

1. **Fetch Data from API**: Make an HTTP request to the provided API endpoint
2. **Parse JSON Response**: Handle the returned JSON data
3. **Display Data**: Create HTML elements to show the information on the page
4. **Handle States**: Implement loading states and error handling
5. **User Interaction**: Make the "Load Data" and "Clear Data" buttons functional

### API Endpoint

Use the following **production API endpoint** for this challenge:

```
https://jsonplaceholder.typicode.com/users
```

This API returns an array of user objects. Each user object contains the following structure:

```json
{
  "id": 1,
  "name": "Leanne Graham",
  "username": "Bret",
  "email": "Sincere@april.biz",
  "address": {
    "street": "Kulas Light",
    "suite": "Apt. 556",
    "city": "Gwenborough",
    "zipcode": "92998-3874",
    "geo": {
      "lat": "-37.3159",
      "lng": "81.1496"
    }
  },
  "phone": "1-770-736-8031 x56442",
  "website": "hildegard.org",
  "company": {
    "name": "Romaguera-Crona",
    "catchPhrase": "Multi-layered client-server neural-network",
    "bs": "harness real-time e-markets"
  }
}
```

## 🛠️ Technical Requirements

### Must Have
- [ ] Use `fetch()` API to retrieve data from the endpoint
- [ ] Display at least the following user information:
  - Name
  - Email
  - Phone
  - City
  - Company name
- [ ] Show a loading state while data is being fetched
- [ ] Handle and display error messages if the API call fails
- [ ] "Load Data" button should fetch and display the data
- [ ] "Clear Data" button should remove displayed data and reset the interface

### Nice to Have
- [ ] Add smooth transitions/animations
- [ ] Create a responsive card layout for each user
- [ ] Add user avatar placeholders
- [ ] Include pagination or "show more" functionality
- [ ] Add data filtering or search functionality

## 🚀 Getting Started

1. **Open the HTML file**: Simply double-click `index.html` to open it in your browser (no server required!)

2. **Open Developer Tools**: Press F12 or right-click → "Inspect" to access the console for debugging

3. **Start Coding**: All your JavaScript code should go in the `<script>` section at the bottom of `index.html`

4. **Test Your Implementation**: Use the buttons to test your API integration

## 💡 Implementation Hints

### Basic Fetch Example
```javascript
async function loadUsers() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/users');
        const users = await response.json();
        // Process and display users
    } catch (error) {
        // Handle errors
    }
}
```

### DOM Manipulation Example
```javascript
// Create a user card
function createUserCard(user) {
    const card = document.createElement('div');
    card.className = 'bg-white border rounded-lg p-4 shadow-sm';
    card.innerHTML = `
        <h3 class="font-semibold text-lg">${user.name}</h3>
        <p class="text-gray-600">${user.email}</p>
        <!-- Add more user information -->
    `;
    return card;
}
```

### State Management Tips
- Use the existing loading div (`#loadingState`) - toggle the `hidden` class
- Use the existing error div (`#errorState`) - update `#errorMessage` with error details
- Replace content in `#dataContainer` for displaying results

## ✅ Evaluation Criteria

Your solution will be evaluated based on:

### Functional Requirements (60%)
- [ ] Successfully fetches data from the API
- [ ] Displays user information clearly and completely
- [ ] Loading states work correctly
- [ ] Error handling is implemented
- [ ] Buttons function as expected

### Code Quality (25%)
- [ ] Clean, readable code with appropriate comments
- [ ] Proper error handling and edge cases
- [ ] Good function/variable naming
- [ ] Efficient DOM manipulation

### User Experience (15%)
- [ ] Intuitive and user-friendly interface
- [ ] Responsive design that works on different screen sizes
- [ ] Smooth interactions and transitions
- [ ] Proper visual hierarchy and information display

## 🎨 Design Guidelines

- The HTML already includes Tailwind CSS for styling
- Try to maintain the existing design aesthetic
- Use the provided color scheme (blues and grays)
- Make sure your data display is clean and organized
- Consider using cards, lists, or tables for data presentation

## ⏰ Time Expectation

This challenge is designed to take approximately **30-60 minutes** to complete the basic requirements, with additional time for enhancements.

## 🆘 Need Help?

If you get stuck:
1. Check the browser console for any JavaScript errors
2. Review the API response structure by testing the endpoint in your browser
3. Make sure you're using the correct element IDs from the HTML
4. Verify that you're handling promises correctly with async/await or .then()

## 📝 Submission

When you're finished:
1. Test your implementation thoroughly
2. Make sure the code is clean and commented
3. Ensure it works by opening `index.html` directly in a browser
4. Be prepared to explain your approach and any challenges you faced

---

**Good luck with your API Integration Challenge!** 🚀

Remember: The goal is to demonstrate your understanding of JavaScript fundamentals, API integration, and DOM manipulation. Focus on making it work first, then enhance the user experience if time permits.