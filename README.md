# Run Llama Locally
Before moving forward, make sure you have atleast 6GB of ram in your Android device to move forward.

To install the llama locally follow the below steps
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
ollama serve &
```
