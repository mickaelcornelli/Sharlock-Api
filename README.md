
# Sharlock API ![sharlockLogo](https://user-images.githubusercontent.com/73282517/176868351-755a43ad-1ae7-4b5d-afa9-aaa74044c427.png)

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
      .then(response => { 
	console.log(response)
      })
      .catch(error => {
      	console.log(error.response)
      });
```
#### Case when you forget to insert partner token
![empty api key insert](https://user-images.githubusercontent.com/73282517/176867433-3e8024af-5c85-49d9-8cdb-96e3d3817b74.png)

#### Case when your token is wrong
![wrong api key](https://user-images.githubusercontent.com/73282517/176867750-47674800-eb8b-4880-96de-0448e6a5359b.png)

#### Case when user password or email is wrong
![wrong pass or email](https://user-images.githubusercontent.com/73282517/176867522-a6fc2586-998e-4731-b6c4-02bf65a9aeee.png)

#### Valid case
![valid case](https://user-images.githubusercontent.com/73282517/176867625-6fa6caaa-6d1c-4dee-b5ea-eab44b7583a8.png)
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

