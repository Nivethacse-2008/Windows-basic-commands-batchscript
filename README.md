# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 

# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT


<img width="353" height="92" alt="Screenshot 2026-05-16 134157" src="https://github.com/user-attachments/assets/ba298516-70b6-4026-ac76-765d2f673005" />


Remove the directory "my-folder"

## COMMAND AND OUTPUT


<img width="306" height="80" alt="Screenshot 2026-05-16 134218" src="https://github.com/user-attachments/assets/5d114e2d-bf4f-48ea-a454-8d1cf12a8b60" />


Create the file Rose.txt

## COMMAND AND OUTPUT


<img width="365" height="87" alt="Screenshot 2026-05-16 134240" src="https://github.com/user-attachments/assets/2e2278a2-520d-49ac-a2d9-10180b4967e8" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT


<img width="453" height="92" alt="Screenshot 2026-05-16 134317" src="https://github.com/user-attachments/assets/62499325-d914-4411-89ab-72fe7ef8504e" />


Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT


<img width="459" height="104" alt="Screenshot 2026-05-16 134447" src="https://github.com/user-attachments/assets/9a7471e3-11bf-43dc-a5ef-6f14b43beb09" />


Remove the file hello1.txt

## COMMAND AND OUTPUT


<img width="367" height="101" alt="Screenshot 2026-05-16 134511" src="https://github.com/user-attachments/assets/d3862f77-8456-41a5-ae7b-45bca576f53b" />


List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT


<img width="430" height="188" alt="Screenshot 2026-05-16 134618" src="https://github.com/user-attachments/assets/5f574f58-b5bc-4930-b9f3-4a87789de196" />


List out all the associated file extensions 

## COMMAND AND OUTPUT


<img width="392" height="221" alt="Screenshot 2026-05-16 134743" src="https://github.com/user-attachments/assets/15ef95be-a042-4000-aa82-2a066084f97e" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT


<img width="399" height="142" alt="Screenshot 2026-05-16 134824" src="https://github.com/user-attachments/assets/7b8c644b-a15a-4cfa-9e88-04ae4eca3a1e" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

PROGRAM

@echo off
set name=John
echo Hello, %name%
pause

## OUTPUT


<img width="389" height="134" alt="Screenshot 2026-05-16 135142" src="https://github.com/user-attachments/assets/c707dc3a-cb4a-4206-8766-078cac31ed92" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.

PROGRAM

@echo off

:START

set /p num=Enter a number: 

set /a rem=%num% %% 2

if %rem%==0 (
    echo The number is Even
) else (
    echo The number is Odd
)

set /p choice=Do you want to continue (Y/N)? 

if /I "%choice%"=="Y" goto START
if /I "%choice%"=="N" goto END

echo Invalid Input
goto START

:END
echo Thank You
pause

## OUTPUT



<img width="469" height="202" alt="Screenshot 2026-05-16 140400" src="https://github.com/user-attachments/assets/f3588b4e-d444-4af6-9dd9-51fbeab5ffe8" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.

PROGRAM

@echo off

for /L %%i in (1,1,5) do (
    echo Number: %%i
)

pause

## OUTPUT



<img width="358" height="158" alt="Screenshot 2026-05-16 140537" src="https://github.com/user-attachments/assets/0362ba60-c656-44c9-840b-a0c96e959187" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

PROGRAM

@echo off

if exist sample.txt (
    echo sample.txt exists
) else (
    echo sample.txt does not exist
)

pause

## OUTPUT


<img width="394" height="89" alt="Screenshot 2026-05-16 140636" src="https://github.com/user-attachments/assets/dad46bc6-fd17-4cd0-b6ff-019e9d0fd096" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

PROGRAM
\@echo off

:MENU
echo ====================
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
echo ====================

set /p choice=Enter your choice: 

if %choice%==1 goto HELLO
if %choice%==2 goto CREATE
if %choice%==3 goto EXIT

echo Invalid Choice
goto MENU

:HELLO
echo Hello, World!
pause
goto MENU

:CREATE
echo This is a new file > newfile.txt
echo File Created
pause
goto MENU

:EXIT
echo Goodbye
pause
exit

## OUTPUT


<img width="485" height="184" alt="Screenshot 2026-05-16 140750" src="https://github.com/user-attachments/assets/09b4b7f9-de47-4367-afc1-05b682521c59" />


# RESULT:
The commands/batch files are executed successfully.

