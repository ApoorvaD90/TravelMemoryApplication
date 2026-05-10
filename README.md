# TravelMemoryApplication
This repository aims to deploy a travel memory app on AWS using multiple EC2 instances for both backend and frontend, with Nginx for reverse proxy, Load Balancers and Target Groups for accurate load distribution, Cloudflare and GoDaddy for public domain access

# Documentation and Screenshots for Travel memory application
All the screenshots and steps for the assignment are added to the word document with title 'Documentation_for_TravelMemory_App'

## Request Flow

The flow of the request is as follows:

1. The request originates from the **Browser**.
2. The request is routed through **Cloudflare**, which provides access to the public domain.
3. Cloudflare forwards the request to the **FE AWS Load Balancer**.
4. The **FE AWS Load Balancer** routes the request to the **FE Target Group**.
5. The **FE Target Group** forwards the request to the **FE instances**.
6. The **FE instances** access the **BE AWS Load Balancer**, which is configured within the FE application/environment.
7. The **BE AWS Load Balancer** routes the request to the appropriate **BE Target Group**.
8. The **BE Target Group** forwards the request to the backend instances.
9. The **BE instances** access **MongoDB** to fetch and update application data.
10. The response is returned back through the application flow and rendered on the **Browser**.

# Architecture Diagram
![Architecture Diagram](/TravelMemoryApplicationArchitecture.drawio.png)
