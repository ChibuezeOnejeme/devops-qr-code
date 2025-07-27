# Use the official Python 3.9 image as the base image
FROM python:3.9

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the requirements.txt file into the container
COPY requirements.txt ./

# Install the required Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy all application files from the current directory to the container
COPY . .

# Set the command to run your FastAPI app using uvicorn
# --host 0.0.0.0 allows external access
# --port 80 exposes the app on port 80
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
