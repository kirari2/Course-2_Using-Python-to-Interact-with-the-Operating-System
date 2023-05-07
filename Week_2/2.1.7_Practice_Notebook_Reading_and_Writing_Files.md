## Practice Notebook: Reading and Writing Files

In this exercise, we will test your knowledge of reading and writing files by playing around with some text files.

Let's say we have a text file containing current visitors at a hotel. We'll call it, *guests.txt*. Run the following code to create the file. The file will automatically populate with each initial guest's first name on its own line.

```python
guests = open("guests.txt", "w")
initial_guests = ["Bob", "Andrea", "Manuel", "Polly", "Khalid"]

for i in initial_guests:
    guests.write(i + "\n")
    
guests.close()
```

No output is generated for the above code cell. To check the contents of the newly created guests.txt file, run the following code.

```python
with open("guests.txt") as guests:
    for line in guests:
        print(line)
```

The output shows that our *guests.txt* file is correctly populated with each initial guest's first name on its own line. Cool!

Now suppose we want to update our file as guests check in and out. Fill in the missing code in the following cell to add guests to the guests.txt file as they check in.

```python
new_guests = ["Sam", "Danielle", "Jacob"]

with open("guests.txt", "a") as guests:
    for i in new_guests:
        guests.write(i + "\n")

guests.close()
```
To check whether your code correctly added the new guests to the guests.txt file, run the following cell.

```python
with open("guests.txt") as guests:
    for line in guests:
        print(line)
```
