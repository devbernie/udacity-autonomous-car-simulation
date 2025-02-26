### **Giới thiệu dự án: Udacity Autonomous Car Simulation**

Dự án **Udacity Autonomous Car Simulation** được xây dựng để mô phỏng và điều khiển xe tự lái trong môi trường giả lập của Udacity. Dự án này sử dụng **mạng nơ-ron tích chập (CNN)** để nhận diện và dự đoán góc lái từ hình ảnh camera của xe trong môi trường mô phỏng.

Dự án có thể chạy trên **Udacity Self-Driving Car Simulator** và được triển khai bằng Python, kết hợp với các thư viện như **Keras, TensorFlow, OpenCV, NumPy** để xử lý dữ liệu và huấn luyện mô hình.

* * * * *

### **Phân tích mã nguồn trong `bright_Untitled6.ipynb`**

Mã nguồn trong notebook này có các bước chính sau:

1.  **Nạp dữ liệu & Tiền xử lý**

    -   Đọc dữ liệu từ tập tin `driving_log.csv`, chứa đường dẫn ảnh, góc lái và thông tin vận tốc.
    -   Tiền xử lý hình ảnh: cắt bỏ phần không cần thiết, chuyển sang thang độ xám, chuẩn hóa dữ liệu.
2.  **Tạo mô hình mạng nơ-ron tích chập (CNN)**

    -   Dựa trên kiến trúc **NVIDIA's End-to-End Learning for Self-Driving Cars**.
    -   Mô hình có nhiều lớp Convolutional, MaxPooling và Fully Connected.
    -   Sử dụng hàm kích hoạt **ReLU**, giảm thiểu overfitting với Dropout.
3.  **Huấn luyện mô hình**

    -   Dữ liệu được chia thành tập huấn luyện và tập kiểm tra.
    -   Sử dụng **Adam Optimizer** với `mean squared error (MSE)` làm hàm mất mát.
    -   Lưu lại mô hình đã được huấn luyện.
4.  **Dự đoán và điều khiển xe**

    -   Mô hình dự đoán góc lái từ hình ảnh camera khi chạy trên trình giả lập.
    -   Kết nối với simulator qua `drive.py` để điều khiển xe theo thời gian thực.

* * * * *

### **Cách sử dụng**

Để chạy dự án, bạn làm theo các bước sau:

#### **1\. Clone repository**

Mở terminal hoặc cmd, chạy lệnh:

```
git clone https://github.com/devbernie/udacity-autonomous-car-simulation.git
cd udacity-autonomous-car-simulation

```

#### **2\. Tải Udacity Self-Driving Car Simulator**

Tải phần mềm mô phỏng từ repository chính thức của Udacity:

```
git clone https://github.com/udacity/self-driving-car-sim.git

```

Sau khi tải xong, di chuyển thư mục `self-driving-car-sim` vào thư mục đã clone.

#### **3\. Cài đặt các thư viện cần thiết**

Chạy lệnh sau để cài đặt các thư viện cần thiết:

```
pip install tensorflow keras numpy opencv-python pandas flask socketio eventlet

```

#### **4\. Khởi chạy mô phỏng**

Mở phần mềm mô phỏng Udacity và chọn chế độ **"Autonomous Mode"**, sau đó chạy lệnh:

```
python drive.py

```

Mô hình sẽ bắt đầu điều khiển xe tự động trên simulator.

* * * * *

### **Tóm tắt**

Dự án **Udacity Autonomous Car Simulation** sử dụng **mô hình CNN** để huấn luyện xe tự lái trong môi trường giả lập. Người dùng có thể tải xuống phần mềm mô phỏng từ Udacity, đặt vào thư mục dự án, sau đó khởi chạy xe với **Python**. Dự án áp dụng **Deep Learning** để xử lý ảnh và điều khiển xe theo thời gian thực.



### **Introduction to the Udacity Autonomous Car Simulation Project**

The **Udacity Autonomous Car Simulation** project is designed to simulate and control a self-driving car in Udacity's simulation environment. This project uses a **Convolutional Neural Network (CNN)** to recognize and predict steering angles from the car's camera images in the simulated environment.

The project runs on the **Udacity Self-Driving Car Simulator** and is implemented in Python, leveraging libraries such as **Keras, TensorFlow, OpenCV, and NumPy** for data processing and model training.

* * * * *

### **Source Code Analysis in `bright_Untitled6.ipynb`**

The notebook contains the following key steps:

1.  **Data Loading & Preprocessing**

    -   Reads data from the `driving_log.csv` file, which includes image paths, steering angles, and speed information.
    -   Preprocesses images by cropping unnecessary parts, converting them to grayscale, and normalizing the data.
2.  **Building the Convolutional Neural Network (CNN) Model**

    -   Based on **NVIDIA's End-to-End Learning for Self-Driving Cars** architecture.
    -   The model consists of multiple **Convolutional, MaxPooling, and Fully Connected layers**.
    -   Uses **ReLU activation function** and applies Dropout to reduce overfitting.
3.  **Training the Model**

    -   Splits data into training and validation sets.
    -   Uses **Adam Optimizer** with `Mean Squared Error (MSE)` as the loss function.
    -   Saves the trained model.
4.  **Prediction & Autonomous Driving**

    -   The trained model predicts the steering angle from real-time camera images.
    -   Connects with the simulator through `drive.py` to control the car autonomously.

* * * * *

### **How to Use**

To run the project, follow these steps:

#### **1\. Clone the Repository**

Open a terminal or command prompt and run:

```
git clone https://github.com/devbernie/udacity-autonomous-car-simulation.git
cd udacity-autonomous-car-simulation

```

#### **2\. Download the Udacity Self-Driving Car Simulator**

Download the simulator from the official Udacity repository:

```
git clone https://github.com/udacity/self-driving-car-sim.git

```

After downloading, move the `self-driving-car-sim` folder into the cloned project directory.

#### **3\. Install Required Libraries**

Run the following command to install the necessary dependencies:

```
pip install tensorflow keras numpy opencv-python pandas flask socketio eventlet

```

#### **4\. Start the Simulation**

Launch the Udacity simulator and select **"Autonomous Mode"**, then run:

```
python drive.py

```

The trained model will start controlling the car in real-time within the simulator.

* * * * *

### **Summary**

The **Udacity Autonomous Car Simulation** project utilizes **a CNN model** to train and operate a self-driving car within a simulated environment. Users can download the Udacity simulator, place it in the project directory, and run the car using **Python**. This project applies **Deep Learning** techniques for real-time image processing and autonomous vehicle control.
