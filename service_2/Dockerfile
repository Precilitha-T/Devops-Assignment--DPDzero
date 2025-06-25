FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Install curl and unzip
RUN apt-get update && apt-get install -y curl unzip

# Download and install uv (as root in Docker)
RUN curl -Ls https://astral.sh/uv/install.sh | bash

# Move uv to a path that Docker can use
ENV PATH="/root/.local/bin:${PATH}"

# Copy all source files
COPY . .

# Install dependencies using uv
RUN uv venv && uv pip install -r requirements.txt

# Expose your service port
EXPOSE 8002

# Run the app
CMD ["uv", "run", "app.py"]
