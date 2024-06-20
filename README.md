````markdown
# Document Chat Bot Setup Guide

This guide provides step-by-step instructions to set up and run the Document Chat Bot. Follow these steps to create the environment, install dependencies, set up API keys, and run the backend and frontend services.

## Prerequisites

Ensure you have the following installed on your machine:

- Python 3.8 or higher
- pip (Python package installer)
- MongoDB
- Streamlit

## Setup Instructions

### 1. Create the Environment and Install Dependencies

Create a virtual environment and activate it:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```
````

Install the required packages:

```bash
pip install -r requirements.txt
```

### 2. Set Up OpenAI API Key, AWS S3 Storage Key, and MongoDB Connection

In `Backend.py` add your OpenAI API key, AWS S3 Storage key, and MongoDB connection string. The code should look like this:

```env
OPENAI_API_KEY=your_openai_api_key
S3_KEY=your_aws_access_key_id
S3_SECRET=your_aws_scret_key_id
S3_BUCKET=your_aws_bucket_key_id
S3_REGION=your_region
S3_PATH=your_S3_path
MONGODB_URI=mongodb://username:password@host:port/database
```

### 3. Run the Backend

Run the backend server by executing the `Backend.py` file:

```bash
python Backend.py
```

### 4. Set the Backend URL in the Frontend

In `Frontend.py`, set the backend URL to point to the server running `Backend.py`. Update the following line in `Frontend.py`:

```python
backend_url = "http://localhost:8000"  # Change to your backend URL if necessary
```

### 5. Run the Frontend

Finally, run the frontend using Streamlit:

```bash
streamlit run Frontend.py
```

## Conclusion

Your Document Chat Bot should now be up and running. Access the frontend through the URL provided by Streamlit to interact with your bot.

If you encounter any issues or need further assistance, please refer to the documentation or raise an issue in the project repository.

Happy Coding!

```

This single file README provides all the necessary setup instructions in one place for easy reference.
```
