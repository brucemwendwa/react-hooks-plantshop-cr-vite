# Plantsy

Plantsy is a React plant shop admin app. It loads plant inventory from a local JSON backend, lets users add new plants, marks individual plants as sold out in the current session, and filters the plant list by name.

## Screenshot

![Plantsy app demo](./demo.gif)

## Features

- Fetches all plants from `http://localhost:6001/plants` when the app loads.
- Adds new plants with a controlled form and persists them with a `POST /plants` request.
- Updates the displayed plant list immediately after a successful create response.
- Marks a plant as `Out of Stock` without persisting that temporary UI state.
- Filters plants by name with a case-insensitive search input.

## Tech Stack

- React
- Vite
- JSON Server
- Vitest
- React Testing Library

## Getting Started

Install dependencies:

```bash
npm install
```

Start the backend:

```bash
npm run server
```

Start the React development server in a second terminal:

```bash
npm run dev
```

Open the app at the local URL printed by Vite. The backend runs at `http://localhost:6001/plants`.

## Testing

Run the included test suite:

```bash
npm run test -- --run
```

## API

`GET /plants` returns the full plant collection.

`POST /plants` creates a plant. Requests should include:

```json
{
  "name": "Plant name",
  "image": "Image URL",
  "price": "10"
}
```
