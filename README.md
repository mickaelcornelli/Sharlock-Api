
# Sharlock API

The sharlock API allows our partners to retrieve information from customers who connect to partner's site through our API.
A token is required to validate that you are a Sharlock's partner, otherwise the API will not return any customer information
## Tech Stack

**Server:** Node, Express


## API Reference

#### Connect user and fetch data

```https://sharlock.herokuapp.com/
  POST /api/v1/signIn
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `data` | `object` | **Required**. Email and password |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your token key |




## Usage/Examples

```javascript
const data = { 
    email: email, 
    password: password 
}

axios
    .post("https://sharlock.herokuapp.com/api/v1/signIn", data, {
        headers: { "x-access-token": "YOUR TOKEN" },
      })
      .then((response) => {
          console.log(response)
      })
      .catch((err)=>{
          console.log(err)
      })
```


## 🚀 About Me
I'm a full stack developer working for Sharlock
- [@mickaelcornelli](https://github.com/mickaelcornelli)



# Hi, I'm Mickael! 👋


## 🛠 Skills
React, React-Native, Firebase, Node, MySQL, Javascript...


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://mickaelcornelli.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mickaël-cornelli/)
- [@mickaelcornelli](https://github.com/mickaelcornelli)
## Support

For support, email tanguimoulin@gmail.com or baptsitemoulinlyon@gmail.com

