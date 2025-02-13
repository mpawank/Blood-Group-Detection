# Blood Group Identification Using OpenCV and Django

This project is a web application built with Django that identifies blood groups by analyzing uploaded blood cell images using OpenCV. The system uses advanced image processing techniques to classify blood groups (A, B, AB, O) along with their positive and negative types.

---

## Features
- Upload blood cell images to identify blood groups.
- Classifies blood groups into A, B, AB, and O, including positive and negative types.
- User authentication (Login/Signup).
- Responsive and modern UI with animations.

---

## Technologies Used
- **Frontend:** HTML, CSS, JavaScript
- **Backend:** Django, Python
- **Image Processing:** OpenCV
- **Database:** SQLite (Default, but can be configured to other databases)

---

## How Blood Group Detection Works

Blood group detection using image processing involves:

1. **Image Preprocessing:**  
   Convert the image to grayscale, apply Gaussian blur for noise reduction, and enhance the contrast.
   
2. **Segmentation:**  
   Segment the regions of interest (A, B, D regions) by splitting the image.

3. **Agglutination Detection:**  
   Detect agglutination (clumping) patterns in each region to identify blood type (A, B, AB, O) and Rh factor (positive/negative).

4. **Classification:**  
   Based on the agglutination detected, classify the blood group and determine if it's positive or negative.

---

## Installation

Follow these steps to set up the project locally:

1. Clone the repository:
  
   git clone <your-repository-url>
   cd blood-group-identification
2. Create a virtual environment:

python -m venv venv

3. Activate the virtual environment:

---On Windows:
venv\Scripts\activate
---On macOS/Linux:
source venv/bin/activate

4. Install the required dependencies:

pip install -r requirements.txt

5. Set up your database:

python manage.py migrate

6. Create a superuser for accessing the admin panel:

python manage.py createsuperuser

7. Run the server:
python manage.py runserver
## Environment Variables
Create a .env file in the project root and define your environment variables. This file will contain secret keys and other configurations for your project. Here's an example:

DEBUG=True
SECRET_KEY=your-secret-key
ALLOWED_HOSTS=localhost,127.0.0.1
Make sure to keep your .env file private and don't commit it to version control.

## Usage
1. Start the server using the command:
python manage.py runserver
Open the browser and go to http://127.0.0.1:8000 to access the web application.

2. Login/Register: Use the login or register functionality to access the blood group detection page.

3. Upload Image: Once logged in, navigate to the profile page and upload an ABO blood cell image.

4. View Results: After uploading the image, the system will process it and display the predicted blood group and Rh factor.

## Contribution Rules
We welcome contributions to this project! If you'd like to contribute, please follow these steps:

1. Fork the Repository
Fork the repository to your own GitHub account by clicking the "Fork" button at the top-right of this page.

2. Create a New Branch
Create a new branch in your forked repository for your feature or fix:
git checkout -b your-branch-name
3. Make Changes
Make your changes in the newly created branch. Ensure that your code follows the coding style and adds tests for new functionality.

4. Commit Changes
Once you've made your changes, commit them:
git add .
git commit -m "Brief description of the changes"
5. Push Changes
Push your changes to your forked repository:
git push origin your-branch-name
6. Create a Pull Request
Create a pull request (PR) from your forked repository to the main repository. Provide a detailed description of the changes you made and why.

## Screenshots
Here are a few screenshots of the application:

Home Page

Blood Group Detection Result

## License
This project is licensed under the MIT License - see the LICENSE file for details.
---

### Summary of the Changes:
1. **All sections are included in a single page**, including installation, usage, contribution rules, and environment variables.
2. **Contribution Rules** section outlines the steps to fork the repo, create a branch, commit changes, and create a pull request (PR).
3. The project’s **usage** and **installation** steps are detailed and should make it easier for contributors and users to set up and contribute to the project.

This `README.md` file should help users and developers easily set up and contribute to the project while also providing a comprehensive guide for usage and setup.









