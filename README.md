# Personal Finance API (from Insight)

The Expense Manager API is a RESTful API designed to manage and track personal expenses. It provides a set of routes for authentication, user profile management, and expense management.

## Authentication

The API uses token-based authentication to secure user data. To access the protected routes, clients must include a valid authentication token in the headers of their HTTP requests.

The following routes are available for authentication:

- GET: /api/auth - Retrieves the Profile of the Current User
- GET: /api/verify/:token - Verifies the Verification Token sent on registration
- POST: /api/auth/login - Login to the API
- POST: /api/auth/register - Register to use the API
- PUT: /api/auth/changePassword - Change Password of the Current User
- PUT: /api/auth/changeIncome - Change monthly income of the Current User
- DELETE: /api/auth/deleteAccount - Permanently Delete the Account of the current user

## Expense Management

The Expense Manager Routes are protected routes that require a valid authentication token to access. They allow users to add, retrieve, modify, and delete their expenses. Additionally, there is a route to generate an excel report of all expenses.

The following routes are available for expense management:

- GET: /api/expense/ - Retrieves all expenses of current user
- GET: /api/expense/:eID - Retrieves the expense with the specific Expense ID
- GET: /api/expense/download/excel - Generates an excel report of all expenses
- POST: /api/expense - Adds a new Expense
- PUT: /api/expense/cancelRecurrance - Converts a Recurring Expense to a Regular one
- DELETE: /api/expense/:eID - Deletes the Expense with the specified Expense ID

## Getting Started

To get started with the Expense Manager API, follow these steps:

1. Clone the repository to your local machine.
2. Install the dependencies using `npm install`.
3. Set up the environment variables in a `.env` file. You will need to define the following variables:
   - `DATABASE_URL` - the URL for your MongoDB database.
   - `JWT_SECRET` - the secret key for your JWT token.
4. Run the application using `npm start`.

You should now be able to access the Expense Manager API on `http://localhost:3000`.

## Conclusion

The Personal Finance API provides a simple and convenient way to manage personal expenses. By integrating this API into a personal finance application, users can easily track their expenses and gain insight into their spending habits.
