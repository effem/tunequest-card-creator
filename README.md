# IMPORTANT
Using the Spotify API to create Games like e.g. [Games or trivia quizzes is against the their terms and conditions](https://developer.spotify.com/compliance-tips#disallowed-use-cases). Therefore, use/host it at your own risk.

# TuneQuest Card Template Creator

The [TuneQuest](https://github.com/effem/tunequest) card template creation tool! 
You can easily generate printable playing card templates for TuneQuest using your favorite Spotify playlists.

Here's how it works:

1. Import Spotify Playlists: Simply provide the URLs of your Spotify playlists containing tracks you want to include in your TuneQuest game.
2. Automatic Track Extraction: Our tool will automatically read the tracks from your playlists and organize them into a printable card template format.
3. Generate PDF Templates: With just a few clicks, generate high-quality PDF templates ready for printing. Each card will display essential track information such as artist, track, and release year on one side and the qr code on the backside.
4. Print and Play: Once you have your PDF templates, simply print them out, cut along the guidelines, and start playing TuneQuest with your friends and family!

## Important Notes
This tool uses the Spotify API to read the release year of the tracks by looking at the tracks album release year. 
When creating your playlist you need to pay attention to select the original tracks and not the remastered versions or version of the tracks that are part of some compilations since this results in wrong release year information.

## Printing the Cards
When printing the cards, make sure to print them duplex and flip on the long edge.
The alignment of the front and backside of the cards depends on the printer and the printer settings.
There are some tolerances in the design to account for slight misalignments.
When selecting your playlist, make sure to select a playlist with a reasonable amount of tracks since only 12 cards fit on one page.

## Getting Started
If you want to run this project, you need to create a `.env` file in the root of the project with the following content:

```env
VITE_SPOTIFY_CLIENT_ID=
VITE_SPOTIFY_REDIRECT_URI=http://localhost:5173
```

To run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

To build the project:

```bash
npm run build
# or
yarn build
# or
pnpm build
# or
bun build
```


## Docker

Use the provided `docker-compose.yaml` file to run the docker image.

```bash
npm run build
docker-compose up -d
```

# TODO
- [ ] Add a loading spinner when fetching the tracks
- [ ] Add a loading spinner when generating the PDF
- [ ] Add a loading spinner when setting the name
- [ ] Add customizations for the card template
