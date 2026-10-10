# country-borders

A world country map for deciding which country a GPS fix or photo was taken in,
published as required by its licence.

`earth.geojson` is one feature per country or territory (`properties.admin`), in WGS 84.

## Source and changes

- **Borders:** © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors,
  via the [Overture Maps Foundation](https://overturemaps.org) `divisions` theme
  (`division_area`, `class = land`), release `2026-09-23.1`.
- **Changes we made:**
  - Simplified to a 5 m tolerance (Douglas-Peucker, shapes kept).
  - 130 land borders redrawn along the US State Department's
    [Large Scale International Boundaries](https://geodata.state.gov) (LSIB v11.4, public domain),
    where Apple's geocoder agreed with that line far more often than with OpenStreetMap's.
  - Country names and territory groupings from [Natural Earth](https://www.naturalearthdata.com)
    admin-0 (public domain).
  - Disputed areas follow the official US government position.
  - Lakes on a border are split along Overture's water boundaries.
  - Islets under 0.5 km² near their own coast and far from any other country are dropped.
  - Antarctica is removed.

## Licence

This database is made available under the [Open Database License (ODbL) v1.0](LICENSE).
Any rights in its individual contents are licensed under the
[Database Contents License](https://opendatacommons.org/licenses/dbcl/1-0/).
If you use it, credit "© OpenStreetMap contributors" and share any adapted database under the same licence.
