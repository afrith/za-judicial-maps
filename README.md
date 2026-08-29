# South Africa Judicial Maps

This repository contains GIS data related to the areas of jurisdiction of
South African courts.

## Disclaimer

I constructed these datasets from official data published by the Department of
Justice and from official notices in the Government Gazette. I regard this as
official information which should be free in terms of section 34 of the
Constitution and section 12(8)(a) of the Copyright Act. As far as I have any
copyright claim, I release it to the public domain.

I can't guarantee the accuracy of this data and it should not be relied on for
legal purposes. If you need legal assurances, consult a lawyer. I'm not
affiliated with the Department of Justice or any other government authority, and
they have not approved this data. It is also not approved by my employer.

## Magisterial districts

The files named `magisterial_districts.*` represent the boundaries of the
magisterial districts and subdistricts, i.e. the areas over which magistrates'
courts have jurisdiction.

This data has mostly been derived from the KML files published by the Department
of Justice at https://www.justice.gov.za/maps/maps.html. I've cleaned up the
polygons so that they form a clean topology, and modified them in certain cases
as described in the section below. In doing so, I've cross-referenced against
the PDF maps published at that same site, and the official government notices
defining the magisterial districts:

- Eastern Cape: [GoN 931 of 2022](https://www.justice.gov.za/legislation/notices/2022/20220330-gg46132-gon931-Rationalisation-EC.pdf)
- Free State: [GoN 929 of 2022](https://www.justice.gov.za/legislation/notices/2022/20220330-gg46132-gon929-Rationalisation-FS.pdf)
- Gauteng: [GoN 5720 of 2024](https://www.justice.gov.za/legislation/notices/2024/20241220-gg51801gon5720-MD-GP.pdf), amended by [GoN 5988 of 2025](https://www.justice.gov.za/legislation/notices/2025/20250313-gg52273gon5988-Jurisdiction-Booysens-GP.pdf) and [GoN 7352 of 2026](https://www.justice.gov.za/legislation/notices/2026/20260408-gg54464gon7352-MagisterialDistricts-GP.pdf)
- KwaZulu-Natal: [GoN 930 of 2022](https://www.justice.gov.za/legislation/notices/2022/20220330-gg46132-gon930-Rationalisation-KZN.pdf)
- Limpopo: [GoN 5718 of 2024](https://www.justice.gov.za/legislation/notices/2024/20241220-gg51799gon5718-MD-LP.pdf)
- Mpumalanga: [GoN 5719 of 2024](https://www.justice.gov.za/legislation/notices/2024/20241220-gg51800gon5719-MD-MP.pdf)
- North West: [GoN 5762 of 2025](https://www.justice.gov.za/legislation/notices/2025/20250117-gg51923gon5762-MD-NW.pdf)
- Northern Cape: [GoN 409 of 2018](https://www.justice.gov.za/legislation/notices/2018/20180329-gg41552_gon409-MDnc.pdf)
- Western Cape: [GoN 932 of 2022](https://www.justice.gov.za/legislation/notices/2022/20220330-gg46132-gon932-Rationalisation-WC.pdf), amended by [GoN 3559 of 2023](https://www.justice.gov.za/legislation/notices/2023/20230621-gg48837gon3559-ROC-WC.pdf)

### Specific issues

- The DoJ KML file for Mpumalanga has substantially different boundaries than
  the PDF maps and the official government notices. I have recreated the
  boundaries according to the official notices.
- In the DoJ KML file and PDF maps, the boundary between the Matatiele
  subdistrict in the Eastern Cape and the Kokstad subdistrict in KwaZulu-Natal
  diverges in two places from the EC/KZN provincial boundary. The PDF maps on
  the DoJ site also show this divergence. However the point-to-point description
  of the Kokstad subdistrict in the official notice follows the provincial
  boundary, and I have chosen this definition.
- The PDF maps are inconsistent as to whether the Moretele area is included
  in the Madibeng district or the Tshwane district. I have followed the North
  West map which places it in the Madibeng district.
- The KML file is missing the Mthonjaneni subdistrict of King Cetshwayo,
  which it merges with the main seat at Empangeni. I have recreated it.
- The boundary of the Swartruggens subdistrict, according to both the KML file
  and the PDF map, does not include Swartruggens town where the court is
  situated. I have corrected the boundary following the point-to-point
  description in the official notice.
- Several other boundaries in the KML file do not match the PDFs or the official
  notices, and I have modified the data accordingly.
  - Bloemfontein district and Botshabelo subdistrict
  - Johannesburg district and Booysens subdistrict
  - Lenasia and Westonaria subdistricts

## High Court divisions

The files named `high_court_divisions.*` represent the boundaries of the areas
of jurisdiction of the main and local seats of the High Court of South Africa.
These boundaries have been derived from the magisterial district boundaries,
according to the areas described in
[Government Notice 7648 of 2026](https://www.justice.gov.za/legislation/notices/2026/20260702-gg54935gon7648-SupCourts-Jurisdiction.pdf).

The Eastern Cape presented two problems. Firstly the definition of the Bhisho
seat was affected by a printing error in the Government Gazette, so I referred
in addition to the
[report of the Moseneke Committee](https://www.justice.gov.za/maps/2023-Report-Recommendations-Rationalisation_HighCourt.pdf)
on which these definitions were based.

Secondly, the notice split certain magisterial districts between two seats of
the Eastern Cape division, without precisely defining how the district was to
be split. I have tried to follow current and historic boundaries to present a
reasonable result. These cases are:

- Sundays River Valley subdistrict, split between Makhanda and Gqeberha.
- Raymond Mhlaba subdistrict, split between Makhanda and Bhisho.
- Sterkspruit district and Emalahleni and Intsika Yethu subdistricts, split
  between Bhisho and Mthatha.
