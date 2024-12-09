# ImGEN
Android App to convert raster images (.jpg/.png/...) to Scalable Vector Graphic (SVG) file for laster engraving/cutting processing.

This application uses OpenCV and Android's camera & gallery integration to apply various image processing operations. It allows you to select an image (from gallery or camera), adjust parameters (thresholds, blur kernel size, etc.), and then view the processed image with edges highlighted. You can also invert colors (edges and background) with a single button, and finally export the processed result as an SVG file.

## Features

- **Select Image Source**: Choose an image from the gallery or capture a new one using the camera.
- **Parameter Adjustments**: Fine-tune thresholds, blur kernel size, line thickness, and more using interactive SeekBars.
- **Color Inversion**: Quickly invert edge and background colors with a single button.
- **SVG Export**: Save your processed image as an SVG file.
- **OpenCV Integration**: Leverages OpenCV for advanced image processing, including:
  - Bilateral filtering
  - Gaussian blur
  - Canny edge detection
  - Dilation and erosion
- **Responsive UI**: Immediate visual feedback on parameter changes.

## Demo:

![image](https://github.com/user-attachments/assets/e31c9ca6-63fc-49b7-b534-f575134e34ca)

# 

![image](https://github.com/user-attachments/assets/7c89452e-56d5-4f38-af67-d1bd646ab0b5)




## Requirements

- **Android Studio**: Latest stable version.
- **Android SDK**: Minimum SDK level as defined in `build.gradle`.
- **OpenCV for Android**: Add the OpenCV library as a module or dependency to your project.
- **Camera & Storage Permissions**: Make sure to request and handle runtime permissions for camera and file access.

## Setup

1. **Clone the Repo**:  
   ```bash
   git clone https://github.com/SSanchz/ImGEN.git
   cd ImGEN

## Add OpenCV:

Download the OpenCV Android SDK from OpenCV.org.
Import it as a module in Android Studio or include it as a dependency if using a repository.
Sync Project with Gradle Files:
After adding OpenCV, click on "Sync Now" in the Android Studio toolbar.

Configure FileProvider & Permissions:

Ensure AndroidManifest.xml has camera permissions and file provider declarations.
Create file_paths.xml in res/xml as per your file structure.

## Usage:
Select Image: Tap "Select Image" button to choose from gallery or take a photo.
Adjust Parameters: Use the sliders for thresholds, blur, etc. Image updates instantly.
Invert Colors: Press the "Invert Colors" button to swap edge/background colors.
Save SVG: Once satisfied, press "Save SVG" to export your processed image as an SVG.

## Code Overview
MainActivity.kt: Contains the main logic, including:
updateImage() function that handles the image processing pipeline.
Integration with OpenCV filters and transformations.
UI event handlers for selecting images, adjusting parameters, inverting colors, and saving SVG.
OpenCV Integration: Core image transformations rely on OpenCV's Imgproc methods.

### Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License.
