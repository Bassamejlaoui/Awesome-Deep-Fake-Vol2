# Awesome Deep Fake 

*Explore deepfake tech powered by AI. Craft unique content responsibly using free AI tools.*

This repository contains a deep fake project aimed at generating realistic face-swapped videos. The project leverages deep learning models and GPU acceleration to perform face swapping efficiently.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1aMqLwtn_jpTObkNlHJg0kS5FFFTuZafG?usp=sharing)

![image](https://github.com/mejbass/Awesome-Deep-Fake-/assets/130122304/4a2d0739-22e8-4502-b316-d36f9a77b81e)


**Tips for Responsible Deepfake Creation**

- **Consent is Key:** Always obtain explicit consent from individuals whose likenesses you wish to use.
- **Integrity Matters:** Ensure that the content you create is never harmful or defamatory.
- **Purposeful Creation:** Strive to make content that is fun or serves a productive purpose.
- **Reflect Before You Act:** Before publishing or sharing a deepfake video, consider its impact.

This project is a profound opportunity to engage with AI in a way that can illuminate its potential for good. Let's set an example for the responsible use of AI and build a community that prioritizes ethical considerations in all our technological endeavors.

We trust in your judgment and creativity.

***Remember:***

- **Consent is Key**
- **Integrity Matters**
- **Purposeful Creation**
- **Reflect Before You Act**
## Installation

To set up the project, follow these steps:

1. **Check for GPU Availability:**
   ```python
   from IPython.display import clear_output
   import codecs
   import torch

   if torch.cuda.is_available():
     device="cuda"
     !apt-get install nvidia-cuda-toolkit
     print("Using GPU")
   else:
     device="cpu"
     print("Using CPU")
   ```

2. **Clone the Repository:**
   ```python
   giturl = codecs.decode('uggcf://tvguho.pbz/Mnpulfnhef/snprshfvba.tvg','rot_13')
   gitdir = codecs.decode('snprshfvba','rot_13')
   !git clone {giturl}
   %cd /content/{gitdir}
   !python install.py --onnxruntime cuda-11.8 --skip-conda

   clear_output()
   print("Installed!")
   ```

## Running the Project

### Local Gradio Interface

To run the project with a local Gradio interface:

1. **Navigate to the Project Directory:**
   ```python
   import codecs
   gitdir = codecs.decode('snprshfvba','rot_13')
   %cd /content/{gitdir}
   ```

2. **Run the Application:**
   ```python
   if device=="cuda":
     !python run.py --execution-providers cpu cuda
   else:
     !python run.py --execution-providers cpu
   ```

### Local Tunnel

To run the project with a local tunnel for remote access:

1. **Install LocalTunnel:**
   ```python
   !npm install -g localtunnel
   ```

2. **Set Up Local Tunnel:**
   ```python
   import subprocess
   import threading
   import time
   import socket
   import urllib.request

   def iframe_thread(port):
       while True:
           time.sleep(0.5)
           sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
           result = sock.connect_ex(('127.0.0.1', port))
           if result == 0:
               break
           sock.close()

       from colorama import Fore, Style
       print(Fore.GREEN + "\nIP: ", Fore.RED, urllib.request.urlopen('https://ipv4.icanhazip.com').read().decode('utf8').strip("\n"), "\n", Style.RESET_ALL)
       p = subprocess.Popen(["lt", "--port", "{}".format(port)], stdout=subprocess.PIPE)
       for line in p.stdout:
           print(line.decode(), end='')

   threading.Thread(target=iframe_thread, daemon=True, args=(7860,)).start()
   ```

3. **Run the Application:**
   ```python
   !python run.py
   ```

## Through Google Colab

You can access the Refacer through Google Colab by following this link: [refacer_colab.ipynb](https://colab.research.google.com/drive/1aMqLwtn_jpTObkNlHJg0kS5FFFTuZafG?usp=sharing)


## Upload the required files

Upload the respective files to their designated sections and click “Start” (The big Red button at the bottom of the page). This action initiates a process that will “reface” all frames in the video using the provided faces. Please note that this process may take some time.

![image](https://github.com/mejbass/Awesome-Deep-Fake-/assets/130122304/491c3be4-a2b5-467b-9ba4-0abe82e3c07b)

## Done!

Congratulations, you have successfully created your first deepfake video. 

Remember:

- **Consent is Key**
- **Integrity Matters**
- **Purposeful Creation**
- **Reflect Before You Act**

## Refacer Not Working?

If you have difficulty with Refacer, try out these alternative tools.

- [Magic Hour: Generative AI Tools for Video Content Creation](https://magichour.ai)
- [AI Face Swap Online Free: Photo, Video, GIF Face Swap](https://www.vidnoz.com/face-swap.html)
- [Free AI Face Swap Online for Videos & Photos | MioCreate](https://www.miocreate.com/face-swap.html)

Questions? Feedback? Requests? Discord: Samej2023

## Disclaimer for Refacer

> :warning: This software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.

> :warning: This software is intended for educational and research purposes only. It is not intended for use in any malicious activities. The author of this software does not condone or support the use of this software for any harmful actions, including but not limited to identity theft, invasion of privacy, or defamation. Any use of this software for such purposes is strictly prohibited.

> :warning: You may only use this software with images for which you have the right to use and the necessary permissions. Any use of images without the proper rights and permissions is strictly prohibited.

> :warning: The author of this software is not responsible for any misuse of the software or for any violation of rights and privacy resulting from such misuse.

> :warning: To prevent misuse, the software contains an integrated protective mechanism that prevents it from working with illegal or similar types of media.

> :warning: By using this software, you agree to abide by all applicable laws, to respect the rights and privacy of others, and to use the software responsibly and ethically.
