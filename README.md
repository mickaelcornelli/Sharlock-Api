
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
#### Case when you forget to insert partner token
![notoken](https://user-images.githubusercontent.com/73282517/175273360-573c833f-a869-4b55-bb63-bf5890c37aed.png)
#### Case when user password or email is wrong
![email pass incorrect](https://user-images.githubusercontent.com/73282517/175273355-12a55c7d-645e-4f42-9dc2-01f6a6838db6.png)
#### Valid case
![fetch valid](https://user-images.githubusercontent.com/73282517/175273358-9f769e2a-2467-49cc-882c-f503bd4d4b82.png)
## Design code btn
#### HTML
```javascript 
<div class="sharlock-btn">
<p class="sharlock-btn-text">Continuez avec Sharlock</p>
</div>
```

#### CSS
```javascript 
.sharlock-btn{
    width: 403px;
    height: 67px;
    background: linear-gradient(91.45deg, #3300FF 0.28%, #8270EE 96.73%);
    border-radius: 10px;
}
.sharlock-btn-text{
    font-family: 'Geomatrix',sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 22px;
    color: #FFFFFF;
}
```

## Used By

This project is used by the following companies:

- spa.fr

# Hi, I'm Mickael! 👋


## 🚀 About Me
I'm a full stack developer working for Sharlock



## 🛠 Skills
React, React-Native, Firebase, Node, MySQL, Javascript...


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://mickaelcornelli.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mickaël-cornelli/)
- [@mickaelcornelli](https://github.com/mickaelcornelli)
## Support

For support, email tanguimoulin@gmail.com or baptsitemoulinlyon@gmail.com

