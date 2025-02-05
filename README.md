# Unpredictable Cropping with background-size: cover;

This repository demonstrates an uncommon issue with the CSS `background-size: cover;` property.  When applied without careful consideration of the aspect ratio of the background image and its container, it can lead to inconsistent rendering across different browsers and devices.

The `bug.css` file contains the problematic CSS. The `solution.css` file offers a solution.

## Problem

The `cover` keyword scales the background image to cover the entire container, maintaining its aspect ratio while potentially cropping parts of the image.  However, the cropping can be unpredictable if the image and container aspect ratios differ significantly, especially across different screen sizes and resolutions.

## Solution

The best solution is to use explicit width and height values for the background image container. This enables precise control over how the image is scaled and avoids unexpected cropping.

Alternatively, consider using `background-size: contain;` which scales the image to fit within the container without cropping, or use javascript to set the background size.