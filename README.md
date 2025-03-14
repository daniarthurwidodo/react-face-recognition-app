# Setting up your React Face Recognition App

## 1. Create a new React application

```bash
npx create-react-app face-recognition-app
cd face-recognition-app
```

## 2. Install necessary dependencies

```bash
npm install react-webcam
```

## 3. Project Structure

Create the following folder structure:

```bash
mkdir -p src/components src/utils
```

## 4. Copy the component files

Copy the following files from the provided code:
- src/App.js
- src/components/FaceDetector.js
- src/components/FaceSimilarity.js
- src/components/ImageUploader.js
- src/components/WebcamCapture.js
- src/utils/opencvUtils.js

## 5. Add CSS to App.css

Uncomment and use the CSS styles provided in the App.css section of the code.

## 6. Download face detection model

For the face detection to work, you need the Haar Cascade classifier XML file:

```bash
# Create a public/models directory
mkdir -p public/models

# Download the Haar Cascade XML file
curl -o public/models/haarcascade_frontalface_default.xml https://raw.githubusercontent.com/opencv/opencv/master/data/haarcascades/haarcascade_frontalface_default.xml
```

Then update the `FaceDetector.js` file to load the model from the correct path:

```js
// Update this line in FaceDetector.js
faceCascade.load('models/haarcascade_frontalface_default.xml');
```

## 7. Run the application

```bash
npm start
```

Your app should now be running at http://localhost:3000