---
layout: home
---

Authors:
- Bartosz Ciereszyński
- Piotr Zajączkowski
- Filip Drazba
- Mateusz Maksimowicz


### Subject: Better handling of albums with multiple CDs

Description:

Currently, when an album has multiple CDs the current display of them is a bit visually unpleasing.
All tracks are displayed in a list where multiple tracks have the same number.

![image](https://github.com/user-attachments/assets/faa1430b-4af1-48f4-9d38-15c19a908060)

Our goal is to modify this aspect and present tracks in separate sections.

Example acceptance criteria:

![image](https://github.com/user-attachments/assets/778c7155-f362-4a71-8b4b-a399d299373b)


| Provider  | Example of a broken album |
| ------------- | ------------- |
| Spotify  | 2Pac - All Eyez On Me / All This Bad Blood  |
| musicBrainz  | 2Pac - All Eyez On Me  |
| Discogs  | Mozart Requiem (angel cover)  |
| ITunes  | 2Pac - All Eyez On Me (cd's not divided at all)  |

### Where to start

[Track](./packages/core/src/structs/Track.ts) -
[https://github.com/pzajaczkowski/nuclear/blob/master/packages/core/src/structs/Track.ts](https://github.com/pzajaczkowski/nuclear/blob/master/packages/core/src/structs/Track.ts)

[SpotifyClient](./packages/core/src/rest/Spotify.ts) - [https://github.com/pzajaczkowski/nuclear/blob/master/packages/core/src/rest/Spotify.ts](https://github.com/pzajaczkowski/nuclear/blob/master/packages/core/src/rest/Spotify.ts)

TrackList - [https://github.com/pzajaczkowski/nuclear/tree/master/packages/ui/lib/components/GridTrackTable](https://github.com/pzajaczkowski/nuclear/tree/master/packages/ui/lib/components/GridTrackTable)

- [GridTrackTable](./packages/ui/lib/components/GridTrackTable/index.tsx)

- [GridTrackTableRow](./packages/ui/lib/components/GridTrackTable/GridTrackTableRow.tsx)