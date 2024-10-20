# Run Llama Locally on Android
Before moving forward, make sure you have atleast 6GB of ram in your Android device to move forward.

### To install the llama locally follow the below steps
1. Install the Termux app from playstore
2. Install  Proot package, which allows you to have the pseudo root access
```
pkg install proot-distro
```
3. Now install the debian distro
```
proot-distro install debian
```
4. Now login to this virtual environment
```
proot-distro login debian
```
5. To install the Ollama, follow this command
```
curl -fsSL https://ollama.com/install.sh | sh
```
6. Now run the below command to start the server
```
ollama serve &
```
7. Now run the following command to install the llama 3.2 1b locally and infer it
```
ollama run llama3.2:1b
```
# Running Locally on workstation with Ollama and webui
Now we will be running llama 3.2 1b locally on workstation. Make sure that your workstatiosn has atleast 8 GB of Ram.
### Steps to Install and run llama models locally
1. First of all install the Ollama locally
```
curl -fsSL https://ollama.com/install.sh | sh
```
2. Run the Ollama server
```
ollama serve 
```
3. Install the llama 3.2 1b or 3b for inference
```
ollama run llama3.2:1b
```
4. Now make sure that docker is Installed and run the following docker command
```
docker run -d --network=host -p 3000:8080 -e OLLAMA_BASE_URL=http://127.0.0.1:11434 -v open-webui:/app/backend/data --name open-webui2 --restart always ghcr.io/open-webui/open-webui:main
```
