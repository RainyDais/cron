<div align="center">
  
# Cron Library

 ------ A libary by RainyDais ------
<div align="center">
  <img src="Div/div.png" alt="simple divider"/>
</div> 

<div align="left">
  
<details open>
<summary> </summary>

<div align="center">
  
## How it works 

```diff
The Cron Library utilized and provides a simple and efficient way to automate tasks based on specified time intervals
```

##      

# How to use

<div align="left">

<div align="center">
  <img src="Div/1.png" alt="divider"/>
</div> 

* Import the module to use the cron library
   
This can be done by using:

`import cron`

<div align="center">
  <img src="Div/2.png" alt="divider"/>
</div> 

* Define a function

This can be done using:

```python
 def your_function():
print("your_text")
```
The `def your_function():` is what you use to make a function, this function will say `your_text` (this is optinal and can be editied)
Example:

```python
 def Hello_Function():
print("Hello World")
```

<div align="center">
  <img src="Div/3.png" alt="divider"/>
</div> 

* Define a function that will tell you when it runs, this will be told every `x` seconds 

This can be done using:

```python
def time_alert_function(seconds):
  print("I run every {0} seconds!".format(seconds))
```
`{0} = x = time before next message`

Example:
```python
def alert(seconds):
  print("Alert's every {111} seconds!".format(seconds))
```

<div align="center">
  <img src="Div/4.png" alt="divider"/>
</div> 

* Create a function to run every `x` amount of times 

Make a first example function to run every 5 seconds

```python
cron.addJob(example_function, 5)
```

Create a second example function to run every 1 second

```python
cron.addJob(time_alert_function, 1, 1)
```
Currently the `addJob` parameters are; `function, timeout/cron delay, args` (only 1 supported currently)

<div align="center">
  <img src="Div/5.png" alt="divider"/>
</div> 

* How to call your Cron jobs
  
You can use this function:

```python
cron.start()
```
  Option: pass `True` into the function call to make it non-thread blocking

  Example:
```python
cron.start(True)
```
  Default is False or thread blocking.

  This will start your timer fyunction, that will then execute your cron jobs.

<div align="center">
  <img src="Div/6.png" alt="divider"/>
</div> 

* To prevent your program from ending whalst using `non-thread blocking mode`

You can use:
```python
input("\n   Hello, this is the end of the file!\n\n")
```
This will also act as a test to prove `cron.start()` isn't blocking the thread
It contains newline characters so it doesn't get put on the same line as
other print messages that will come in from the threaded cron jobs.
 
</details>
text goes here
