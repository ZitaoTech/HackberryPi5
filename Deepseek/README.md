# Running Deepseek on HackberryPi5  
Note: Ollama can only run with 64-bit OS, so make sure you have installed the 64-bit OS before you install ollama(step3)  

### 1. First update you operate-system  
```sh
sudo apt update
sudo apt upgrade
```

### 2. Ensure that the curl package is available on your Pi.  
```sh
sudo apt install curl
```

### 3. Install the Ollama software on your Pi 
```sh
curl -fsSL https://ollama.com/install.sh | sh
```

### 4. Running Deepseek on your HackberryPi5
```sh
ollama run deepseek-r1:1.5b
```
![image](https://github.com/user-attachments/assets/8201ccb8-dfe7-4a23-b012-5d5d18c0e085)
