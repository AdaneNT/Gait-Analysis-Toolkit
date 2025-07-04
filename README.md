# Gait-Analysis-

Gait analysis (GA) toolkit is a machine learning-based human activity recognition tool developed for detecting common activities of daily living (ADLs), such as walking, jogging, going upstairs, going downstairs, sitting, and standing. The GA toolkit contains a pre-trained model based on the smartphone acceleration dataset obtained from wearable inertial sensors.

## Installation Instructions

The GA toolkit has been packaged in a Dockerized container.

The toolkit’s image can be tested and run on a local machine using the following command:

```bash
docker run -d -p 8082:8080 gait_module
```

Currently, the GA image can also be pulled and tested from Docker Hub by typing the following commands:

- **Step 1:**  
  ```bash
  docker pull adanentnu/gait_module
  ```

- **Step 2:**  
  ```bash
  docker run -p 8088:8080 adanentnu/gait_module
  ```

- **Step 3:**  
  Open your browser and go to:  
  ```
  http://localhost:8088/apidocs
  ```

---

## Update Log

- Minor formatting improvements and addition of an update log.
- Initial version of README created for demonstration of GitHub pull request workflow.
