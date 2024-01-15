# Project Doom Fire Algorithm
This project is a project presented on the YouTube channel of Felipe dechamps reference: https://www.youtube.com/watch?v=HCjDjsHPOco

This project consists of creating the fire animation of the Doom game, released in 1993.

Here is a detailed explanation:

## Variable Initialization

The code begins by initializing an array  `firePixelsArray`  to store the intensity of each pixel in the fire, and two constants  `fireWitdh`  and  `fireHeight`  to define the dimensions of the fire. An array  `fireColorsPalette`  is also defined, which contains objects representing different colors.

## **Start function**

This function is the entry point of the fire effect. It calls the functions  `createFireDataStructure`,  `createFireSource`, and  `renderFire`  to set up the fire. It also sets an interval to call  `calculateFirePropagation`  every 50 milliseconds, which updates the fire effect over time.

## **CreateFireDataStructure function**

 This function initializes  `firePixelsArray`  with zeros. The size of the array is the total number of pixels in the fire, which is the product of  `fireWitdh`  and  `fireHeight`.

## **CalculateFirePropagation function**

 This function iterates over each pixel in the fire and calls  `updateFireIntensityPerPixel`  for each one, then calls  `renderFire`  to update the visual representation of the fire.

## **UpdateFireIntensityPerPixel function**

 This function calculates the new intensity of a pixel based on the intensity of the pixel below it. It introduces a ‘decay’ factor to make the fire look more realistic.

## **RenderFire function**

This function generates an HTML string representing the fire and inserts it into the  `#fireCanvas`  element in the DOM. Each pixel in the fire is represented by a  `td`  element. The color of the pixel is determined by its intensity and the  `fireColorsPalette`.

## **CreateFireSource function**

 This function sets the intensity of the bottom row of pixels in the fire to the maximum value.

## **Start function call**

 Finally, the  `start`  function is called to kick off the fire effect.

The HTML and CSS code at the end of the script is used to style the fire effect and display it on a webpage. The fire effect is displayed in a table, with each cell representing a pixel in the fire. The color of each cell is determined by the fire intensity at that pixel, which is updated over time to create the animation effect.
