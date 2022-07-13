
# ![sharlockLogo](https://user-images.githubusercontent.com/73282517/176868351-755a43ad-1ae7-4b5d-afa9-aaa74044c427.png) Sharlock API

The sharlock API allows our partners to retrieve information from customers who connect to partner's site through our API.
An API KEY is required to validate that you are a Sharlock's partner, otherwise the API will not return any customer information
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
| `token` | `string` | **Required**. Your api key |

#### Reset user password

```https://sharlock.herokuapp.com/
  POST /api/v1/resetPassword
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Email|

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `token` | `string` | **Required**. Your api key |


## Usage/Examples

### Axios
```javascript
const data = { 
    email: email, 
    password: password 
}

axios
    .post("https://sharlock.herokuapp.com/api/v1/signIn", data, {
        headers: { "apikey": "YOUR APIKEY" },
      })
      .then(response => { 
	console.log(response)
      })
      .catch(error => {
      	console.log(error.response)
      });
```
### Fetch
```
 const data = { 
    email: email, 
    password: password 
 }
 const apiURL = "http://localhost:9500/api/v1/signIn"
 const apikey = "Your apikey"

    fetch(apiURL, {
      method: "POST",
      body: JSON.stringify(data),
      headers: {
        "content-type": "application/json",
        'apikey': apikey,
      }
    })
      .then((response) => {
        response.json()
          .then((res) => console.log(res))
          .catch((err) => console.log(err))
      })
      .catch((error) => console.log(error))
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


## FAQ

#### Can I use the api without token or api key ?

In order for partners to write data via the API, we have created a partner specific authentication workflow. Upon being completed successfully, the partner account that is created can be used to fetch data from the client and get all details if the client confirm to send his personnal information like firstname, lastname, age, email etc...

#### Where can i found my API_key ?

You must be a partner to obtain an API key. Visit our website and submit message on our form to be partner.

#### Can I contribute to this API ?

It's not a public API, so you must be a sharlock developper or be in our team to improve API.
Feel free to contact founders of the project on the github support section.

## Support

For support, email tanguimoulin@gmail.com or baptsitemoulinlyon@gmail.com

