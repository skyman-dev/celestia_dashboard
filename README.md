# Grafana Installation Guide for Celestia Node
![image](https://github.com/user-attachments/assets/b1aacb64-d669-4f69-80a0-d9512af25bc6)

## Introduction

This guide provides step-by-step instructions on how to install and set up a Dashboard for monitoring a Celestia node and key hardware performance metrics  
**Note**: It is recommended to install Grafana and Prometheus on a separate server. On the server where your Celestia node is running, install Node Exporter and enable Prometheus in the node configuration. This setup ensures optimal performance and easier management. More details on configuration can be found below.

## Prerequisites

Before you begin, ensure you have the following:

- **Grafana** installed on your system. If not, download it from the [official website](https://grafana.com/docs/grafana/latest/setup-grafana/installation/).
- A configured Prometheus data source for your Node in Grafana, along with the Node Exporter added to collect hardware metrics

## Installation Steps

1. **Access Grafana**

   Open your web browser and navigate to your Grafana instance, typically at `http://<your_ip>:3000`, or use your domain name if a web server is configured.

2. **Import the Dashboard**

   - Click on the **"+"** icon on the left sidebar.
   - Select **"Import"** from the dropdown menu.

3. **Upload the Dashboard**

 Option 1: Upload the JSON File
   - In the **"Import via panel json"** section, click on **"Upload .json File"**.
   - Select the downloaded JSON file.
 Option 2: Import via Dashboard UID
   - In the "Import via panel json" section, enter the Dashboard UID: `22036`.
   - Click "Load" and confirm the dashboard settings.

4. **Configure the Dashboard**

   - Once the JSON is uploaded, Grafana will display the dashboard title and other details.
   - Choose the **Prometheus** **data source** from the dropdown menu if prompted.
   - Click **"Import"** to complete the process.

## Configuration

- **Variables Adjustment**: The dashboard uses variables, so specify the host and port where the Node Exporter is running (default port is 9100)  
!Note: If Node Exporter is not installed on your server, use this [guide](https://medium.com/@abdullah.eid.2604/node-exporter-installation-on-linux-ubuntu-8203d033f69c) to install and configure Node Exporter with Prometheus.
- **Data Source Verification**: Double-check that the dashboard panels are pulling data from the correct data source.

## Usage

- Navigate through the dashboard to view your metrics.
- Customize panels as needed by clicking on the panel title and selecting **"Edit"**.
- Save any changes by clicking on the **"Save"** icon at the top right corner.

## Support

If you encounter any issues or have questions, feel free to open an issue on the [GitHub repository](#).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
