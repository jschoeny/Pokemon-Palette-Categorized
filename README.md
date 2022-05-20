# Pokemon Palette Categorized
  A categorization of the primary and secondary colors of the sprites found in the Pokeemerald Expansion by rh-hideout

  The provided tool is **highly recommended** to make categorization easier.

# Guidelines
- **Submit pull requests to the `dev` branch**
  - Include a screenshot of the front and back images in typings of your choosing, i.e.:
<p align="center">
<img width="100" alt="Tentacruel as a Dark and Electric type" src="https://user-images.githubusercontent.com/2257407/169610991-05f4512f-ba5e-4870-ad53-d01c2c8dd9c7.png"> <img width="100" alt="Tentacruel as a Fairy and Dark type" src="https://user-images.githubusercontent.com/2257407/169612005-db89cab6-328f-46f5-b969-0f27b1e4ed5d.png">
</p>

- Avoid including black in any categories (usually `16 16 16`)
- Use the more prominent colors for the primary category, and less prominent for secondary
- Try to keep similar categories across evolutions
- Try to have the Pokemon look good across as many type-combinations as possible
- Some Pokemon will have colors that cause the primary and secondary categories to conflict, as can be seen with the Poochyena below *(notice the tops of its ears and the fur lines on its side when Fairy/Rock type)*:
  - The .png (and often the .pal) will need to be modified to change the colors at those pixel positions to something being used by the opposite category. **Try to keep the modified image looking as close to the original as possible**
  - An example difference can be seen with this Poochyena:

<table align="center">
  <tr>
    <th align="center">
      <img width="100" alt="Original Poochyena sprite" src="https://user-images.githubusercontent.com/2257407/169617163-7719c9f9-cbd5-4362-8acb-fd3ca71c997a.png">
    </th>
    <th align="center">
      <img width="100" alt="Modified Poochyena sprite" src="https://user-images.githubusercontent.com/2257407/169618443-908fcf6a-89ac-4711-b0c4-02bbe4c881d2.png">
    </th>
    <th align="center">
      <img width="100" alt="Fairy/Rock Original Poochyena sprite" src="https://user-images.githubusercontent.com/2257407/169618541-f11da83d-fa62-415a-9f05-e49d3d65c8e8.png">
    </th>
    <th align="center">
      <img width="100" alt="Fairy/Rock Modified Poochyena sprite" src="https://user-images.githubusercontent.com/2257407/169619207-04095ddb-1e0e-4a3d-bc8c-87bf6a452bd6.png">
    </th>
  </tr>
  <tr>
    <td width="150" align="center">Original sprite</td>
    <td width="150" align="center">Modified sprite</td>
    <td width="150" align="center">Original sprite</td>
    <td width="150" align="center">Modified sprite</td>
  </tr>
</table>

# Formatting
## .pal format
  The indexes of a sprite's color is ordered by its appearance in its .pal file, i.e.:
  ```c
  JASC-PAL
  0100
  16           // # of colors
  152 208 160  // Index 0 (usually background)
  48 80 88     // Index 1
  112 160 144  // Index 2
  16 16 16     // Index 3
  64 120 112   // Index 4
  ...
  ```
## typeCategories.txt format
  ```c
  primaryIndexes
  4   // The number of color indexes
  5   // An index from the sprite's .pal file
  6
  7
  8
  secondaryIndexes
  3   // The number of color indexes
  1   // An index from the sprite's .pal file
  2
  4
  ```
