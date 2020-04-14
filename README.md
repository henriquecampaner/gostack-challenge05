<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Challenge 05: First Node.js project
</h3>

<p align="center">“For those who get better every day, getting ready is utopia”!</blockquote>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/rocketseat/bootcamp-gostack-desafios?color=%2304D361">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%2304D361">
  </a>

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/Rocketseat/bootcamp-gostack-desafios/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/rocketseat/bootcamp-gostack-desafios?style=social">
  </a>
</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">about the challenge</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">License</a>
</p>

## :rocket: About the challenge

In this challenge, you must create an application to continue training what you have learned so far in Node.js with TypeScript, using the concept of models, repositories and services!

This will be an application for storing incoming and outgoing financial transactions, which should allow the registration and listing of these transactions.

### Application routes

Now that you have the template cloned, and ready to continue, you should check the files in the `src` folder and complete where there is no code with the code to achieve the objectives of each route.

- **`POST / transactions`**: The route must receive` title`, `value` and` type` within the body of the request, with `type` being the type of the transaction, which must be` income` for entries ( deposits) and outcome for withdrawals. When registering a new transaction, it must be stored inside an object with the format like the following:

```json
{
  "id": "uuid",
  "title": "Salário",
  "value": 3000,
  "type": "income"
}
```

- **`GET / transactions`**: This route should return a listing with all the transactions that you have registered so far, together with the sum of entries, withdrawals and total credit. This route must return an object with the following format:

```json
{
  "transactions": [
    {
      "id": "uuid",
      "title": "Salary",
      "value": 4000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Freelance",
      "value": 2000,
      "type": "income"
    },
    {
      "id": "uuid",
      "title": "Invoice payment",
      "value": 4000,
      "type": "outcome"
    },
    {
      "id": "uuid",
      "title": "Gamer Chair",
      "value": 1200,
      "type": "outcome"
    }
  ],
  "balance": {
    "income": 6000,
    "outcome": 5200,
    "total": 800
  }
}
```

### Testing specification
In each test, you have a brief description of what your application must do in order for the test to pass.

For this challenge we have the following tests:

- **`should be able to create a new transaction`**: For this test to pass, your application must allow a transaction to be created, and return a json with the created transaction.

- **`should be able to list the transactions`**: In order for this test to pass, your application must allow an object containing all transactions to be returned together with the balance of income, outcome and total transactions that were created up to the time.

- **`should not be able to create outcome transaction without a valid balance`**: In order for this test to pass, your application must not allow a 'outcome` type transaction to exceed the total amount that the user has in cash, returning a response with HTTP 400 code and an error message in the following format: `{error: string}`

## :calendar: Delivery

This challenge must be delivered from the Skylab platform, send the link to the repository where you made your changes. After completing the challenge, making a post on Linkedin and posting the code on Github is a good way to demonstrate your knowledge and efforts to evolve your career for future opportunities.

## :memo: License

This project is under the MIT license. See the [LICENSE] file (LICENSE.md) for more details.

---

Made with 💜 by Rocketseat: wave: [Join our community!] (Https://discordapp.com/invite/gCRAFhc)
