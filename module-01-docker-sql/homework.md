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
<img width="1249" height="342" alt="image" src="https://github.com/user-attachments/assets/0c7d116f-be83-48c1-ac24-002f1c76015e" >

<br>
the output says "pip 25.3 from /usr/local/lib/python3.13/site-packages/pip (python 3.13)". so <b>the answer is 25.3 (a)</b>

# QUESTION 2


# QUESTION 3
For the trips in November 2025, how many trips had a trip_distance of less than or equal to 1 mile? (1 point)
a. 7,853 <br>
b. 8,007 <br>
c. 8,254 <br>
d. 8,421 <br>
