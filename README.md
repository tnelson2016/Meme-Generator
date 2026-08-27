# Meme Generator

A React app for generating memes using random templates from the [Imgflip API](https://imgflip.com/api).

## Features

- Fetches a set of popular meme templates from Imgflip on load
- Enter custom top and bottom text
- Click GEN to overlay your text on a randomly selected template image

## Tech Stack

- React 16.8.6 (Create React App / react-scripts 3.0.0)
- Imgflip `/get_memes` API (public, no API key required)

## Getting Started

This project uses an older version of `react-scripts` that requires Node 16 (newer Node versions will throw an OpenSSL-related build error).

```bash
git clone https://github.com/tnelson2016/Meme-Generator.git
cd Meme-Generator
nvm use 16          # or use NODE_OPTIONS=--openssl-legacy-provider on newer Node
npm install --omit=optional
npm start
```

The app will open at [http://localhost:3000](http://localhost:3000).

## Known Issues

- No styling on the text inputs or GEN button — functional but plain
- No image loading state while memes are being fetched
- No test coverage beyond the default CRA smoke test

## Project Structure

```
src/
  components/
    Header.js          # Page header/banner
    MemeGenerator.js    # Form, meme image, and Imgflip fetch logic
  App.js                 # Root component
```