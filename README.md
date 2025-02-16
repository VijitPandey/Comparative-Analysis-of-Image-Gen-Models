Comparative Analysis of Image
Generation Models
This project utilizes SAM2 for image segmentation, MongoDB for data storage, and an image
generation module. It’s designed to run optimally in a Linux-based environment, preferably
through a WSL terminal, as this helps handle dependencies effectively.
Prerequisites
1. WSL or Linux Environment: Recommended for dependency management.
2. Python: Version 3.8 or higher.
3. MongoDB Compass: To connect to the database.
4. ngrok: For secure tunneling and domain setup.
5. Node.js and npm: Required for running the React frontend.
Project Setup
Step 1: SAM2 Segmentation Model Setup
The project uses the SAM2 model for segmentation. Please follow the build instructions
provided in the repository to set up the SAM2 model.
bash
Copy code
# Clone the SAM2 repository (if not done already)
git clone https://github.com/facebookresearch/sam2.git
cd sam2
# Follow the setup instructions in the README
●●
Note: Ensure all dependencies required by SAM2 are installed, as this model may have
specific requirements.
Step 2: MongoDB Setup
● Database Connection: Open the final_receiver.ipynb file and provide the
connection string for MongoDB Compass.
○ This is used to interact with your database, so make sure it’s correctly set up.
Step 3: ngrok Configuration
1. Create a ngrok account: ngrok allows you to expose your local servers to the internet
securely.
2. Get the Auth Token and Domain Link:
○ Retrieve the authentication token and update the settings in the image.ipynb
file.
○ Set the domain link for public access as specified in your ngrok account.
Step 4: Run the Application
The project includes multiple components, so make sure to run them in the following order for
the application to work smoothly:
1. Start the Servers:
Run app.py, final_receiver.ipynb, and image.ipynb in separate terminals.
bash
Copy code
# Start app.py
python app.py
○
2. React Frontend:
Navigate to the React app directory and start the frontend:
bash
Copy code
cd path/to/react-app
npm install
npm start
○
Final Notes
● Environment Management: For ease of use, consider setting up a virtual environment
for each Python component to manage dependencies.
● Errors and Troubleshooting: Refer to the SAM2 GitHub page for model-specific issues
or consult MongoDB and ngrok documentation if connection issues occur.
