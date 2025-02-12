taskManager.js
const tasks = [];

const addTask = (title, status, priority) => {
    tasks.push({ title, status, priority });
};

const filterByStatus = (status) => tasks.filter(task => task.status === status);

const findHighPriorityTask = () => tasks.find(task => task.priority === 5);

const taskSummaries = () => tasks.map(task => `Task: ${task.title}, Status: ${task.status}`);

const logTasks = () => {
    console.log("Task List:");
    tasks.forEach(task => {
        console.log(`Title: ${task.title}, Status: ${task.status}, Priority: ${task.priority}`);
    });
};

addTask("Complete Assignment", "Pending", 4);
addTask("Buy Groceries", "Completed", 2);
addTask("Prepare Presentation", "Pending", 5);
addTask("Exercise", "Completed", 3);

console.log("Filtered Pending Tasks:", filterByStatus("Pending"));
console.log("High Priority Task:", findHighPriorityTask());
console.log("Task Summaries:", taskSummaries());
logTasks();

taskCartSystem.js
const tasks = [];

const addTask = (title, status, priority) => {
    tasks.push({ title, status, priority });
};

const filterByStatus = (status) => tasks.filter(task => task.status === status);

const findHighPriorityTask = () => tasks.find(task => task.priority === 5);

const taskSummaries = () => tasks.map(task => `Task: ${task.title}, Status: ${task.status}`);

const logTasks = () => {
    console.log("Task List:");
    tasks.forEach(task => {
        console.log(`Title: ${task.title}, Status: ${task.status}, Priority: ${task.priority}`);
    });
};

addTask("Complete Assignment", "Pending", 4);
addTask("Buy Groceries", "Completed", 2);
addTask("Prepare Presentation", "Pending", 5);
addTask("Exercise", "Completed", 3);

console.log("Filtered Pending Tasks:", filterByStatus("Pending"));
console.log("High Priority Task:", findHighPriorityTask());
console.log("Task Summaries:", taskSummaries());
logTasks();

const cart = [];

const addProduct = (productName, price, quantity) => {
    cart.push({ productName, price, quantity });
};

const calculateTotal = () => cart.reduce((total, product) => total + (product.price * product.quantity), 0);

const removeProduct = (productName) => {
    const index = cart.findIndex(product => product.productName === productName);
    if (index !== -1) cart.splice(index, 1);
};

const logCart = () => {
    console.log("Shopping Cart:");
    cart.forEach(({ productName, price, quantity }) => {
        console.log(`Product: ${productName}, Price: $${price}, Quantity: ${quantity}`);
    });
};

addProduct("Laptop", 1200, 1);
addProduct("Mouse", 25, 2);
addProduct("Keyboard", 45, 1);

console.log("Total Cost:", calculateTotal());
logCart();
removeProduct("Mouse");
console.log("Updated Cart:");
logCart();

taskCartWeather.js
const tasks = [];

// Add Task (Arrow Function)
const addTask = (title, status, priority) => {
    tasks.push({ title, status, priority });
};

// Filter by Status
const filterByStatus = (status) => tasks.filter(task => task.status === status);

// Find High Priority Task
const findHighPriorityTask = () => tasks.find(task => task.priority === 5);

// Map Task Titles with Status
const taskSummaries = () => tasks.map(task => `Task: ${task.title}, Status: ${task.status}`);

// Log Task Details
const logTasks = () => {
    console.log("Task List:");
    tasks.forEach(task => {
        console.log(`Title: ${task.title}, Status: ${task.status}, Priority: ${task.priority}`);
    });
};

// Example Usage
addTask("Complete Assignment", "Pending", 4);
addTask("Buy Groceries", "Completed", 2);
addTask("Prepare Presentation", "Pending", 5);
addTask("Exercise", "Completed", 3);

console.log("Filtered Pending Tasks:", filterByStatus("Pending"));
console.log("High Priority Task:", findHighPriorityTask());
console.log("Task Summaries:", taskSummaries());
logTasks();

// Shopping Cart System
const cart = [];

// Add Product
const addProduct = (productName, price, quantity) => {
    cart.push({ productName, price, quantity });
};

// Calculate Total Cost
const calculateTotal = () => cart.reduce((total, product) => total + (product.price * product.quantity), 0);

// Remove Product
const removeProduct = (productName) => {
    const index = cart.findIndex(product => product.productName === productName);
    if (index !== -1) cart.splice(index, 1);
};

// Log Product Details
const logCart = () => {
    console.log("Shopping Cart:");
    cart.forEach(({ productName, price, quantity }) => {
        console.log(`Product: ${productName}, Price: $${price}, Quantity: ${quantity}`);
    });
};

// Example Usage
addProduct("Laptop", 1200, 1);
addProduct("Mouse", 25, 2);
addProduct("Keyboard", 45, 1);

console.log("Total Cost:", calculateTotal());
logCart();
removeProduct("Mouse");
console.log("Updated Cart:");
logCart();

// Weather Forecast Tracker
const cities = [];

// Add City Weather
const addCityWeather = (cityName, temperature, condition) => {
    cities.push({ cityName, temperature, condition });
};

// Find Hottest City
const findHottestCity = () => cities.reduce((hottest, city) => (city.temperature > hottest.temperature ? city : hottest), cities[0]);

// Filter by Condition
const filterByCondition = (condition) => cities.filter(city => city.condition === condition);

// Map City Names with Temperature
const citySummaries = () => cities.map(city => `City: ${city.cityName}, Temp: ${city.temperature}°C`);

// Log Hottest City Details
const logHottestCity = () => {
    if (cities.length === 0) return;
    const { cityName, temperature, condition } = findHottestCity();
    console.log(`Hottest City: ${cityName}, Temperature: ${temperature}°C, Condition: ${condition}`);
};

// Example Usage
addCityWeather("New York", 30, "Sunny");
addCityWeather("London", 22, "Cloudy");
addCityWeather("Dubai", 42, "Sunny");
addCityWeather("Tokyo", 27, "Rainy");

console.log("Filtered Cities (Sunny):", filterByCondition("Sunny"));
console.log("City Summaries:", citySummaries());
logHottestCity();
