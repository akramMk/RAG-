# Use a lightweight Python image
FROM python:3.11-slim

# Set a working directory inside the container
WORKDIR /app

# Copy the requirements file first for dependency installation
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . .

# Expose the port used by Streamlit
EXPOSE 8501

# Default command to run the Streamlit application
CMD ["streamlit", "run", "index.py", "--server.port=8501", "--server.address=0.0.0.0"]
