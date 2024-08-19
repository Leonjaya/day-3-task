# day-3-task
// Use the REST Countries API URL
const apiURL = 'https://restcountries.com/v3.1/all';

// Fetch data from the API
fetch(apiURL)
  .then(response => response.json())
  .then(data => {
    // Loop through the data and display each flag
    data.forEach(country => {
      console.log(country.flags.svg); // Display the flag's URL
    });
  })
  .catch(error => console.error('Error fetching data:', error));
