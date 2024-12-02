Here is how you can structure the steps into a `README.md` file:

```markdown
# Running the App

## 1. Install Dependencies

To install the required dependencies, run the following command:

```bash
pip install -r requirements.txt
```

This will install Flask and any other dependencies listed in the `requirements.txt` file.

## 2. Start Flask App Locally

You can run the Flask app locally for testing using the following command:

```bash
python app.py
```

This will start the app on `localhost` at port `5000`.

## 3. Run the App as a Background Service on EC2

To run the app in the background using a systemd service on an EC2 instance, follow these steps:

### a. Enable the systemd Service

Move the `portfolio.service` file to the systemd directory:

```bash
sudo cp portfolio.service /etc/systemd/system/
```

### b. Reload systemd Daemon

Reload the systemd manager configuration:

```bash
sudo systemctl daemon-reload
```

### c. Start the Service

Start the app service:

```bash
sudo systemctl start portfolio
```

### d. Enable the Service at Boot

Enable the app to start automatically on system boot:

```bash
sudo systemctl enable portfolio
```

## 4. Access the App

You should now be able to access the app by navigating to your EC2 instance's public IP on port `5000`. For example:

```
http://<your-ec2-public-ip>:5000
```

Replace `<your-ec2-public-ip>` with the actual public IP address of your EC2 instance.
```

This `README.md` will help others set up and run the Flask app both locally and on an EC2 instance.