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
