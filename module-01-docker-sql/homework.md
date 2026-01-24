# QUESTION 1
What's the version of pip in the python:3.13 image? <br>
a. 25.3 <br>
b. 24.3.1 <br>
c. 24.2.1 <br>
d. 23.3.1 <br>

### Answer :
I run this command on the github codespace terminal:
````bash
docker run -it --rm -v $(pwd):/app python:3.13 pip -V"
````
the output would be like this :
<img width="1249" height="342" alt="image" src="https://github.com/user-attachments/assets/0c7d116f-be83-48c1-ac24-002f1c76015e" 

the output says "pip 25.3 from /usr/local/lib/python3.13/site-packages/pip (python 3.13)". so **the answer is 25.3 (a)**

# QUESTION 2


# QUESTION 3
