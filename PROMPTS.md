# PROMPTS.md — AI Usage Log
# IIT414W · Tomás Solano · Lab 0

  There were 3 prompts given to ChatGPT

## 1. Requirements.txt:

  > Context: Was trying to create a requirements.txt that had compatible versions with one another, for the most part pip takes care of getting the right versions but while using a requirements.txt you need to at least get minimum version for everything to work.

  > Prompt: 
  ```
  i want to get a requirements.txt with the following libraries for python version 3.10+ that has the necessary dependencies between each other and python for it to work on any version over python 3.10: jupyterlab numpy pandas scikit-learn matplotlib seaborn fastf1 ipykernel
  ```

  > Relevant Output: 
        ``` bash
        jupyterlab>=4.0
        ipykernel>=6.25

        numpy>=1.23
        pandas>=1.5
        scikit-learn>=1.2

        matplotlib>=3.6
        seaborn>=0.12

        fastf1>=3.0
        ```

  > Validation: Tried to run it with pip on a clean install of a new virtual environment and it worked as intended.

  > Adaptations: Didn't change much since it run as intended.

  > Final Decision: Used

## 2. Time formatter
  
  > Context: Needed a way to get a clearer output when working with timedelta data in pandas's DataFrame.

  > Prompt: 
  ```
  How do i pass from timedelta64 to an easier to read number like "54 minutes and 30 seconds": laps_df.groupby("Driver")["LapTime"].std()?
  ```

  > Relevant Output: 
        ``` python
        import pandas as pd

        std_laps = laps_df.groupby("Driver")["LapTime"].std()

        def format_timedelta(td):
            total_seconds = int(td.total_seconds())
            minutes = total_seconds // 60
            seconds = total_seconds % 60
            return f"{minutes} minutes and {seconds} seconds"

        formatted = std_laps.apply(format_timedelta)
        print(formatted)
        ```

  > Validation: Check for what It gave me then created my own version with what I needed.

  > Adaptations: 
        ``` python
        format_time = lambda x: f"{x.total_seconds() % 60} Seconds"
        ```

  > Final Decision: Reference / Partially Used


  ## 3. README cleanup
  
  > Context: Made the REAMDE.md but felt like it could use some cleanup in some areas to improve readability

  > Prompt: 
  ```
  1. Have to do a readme for all of this, and already did, however I think the readme needs a bit of a cleaning for clearer understanding, can you help me check on that? <README.MD>
  2. can you give me the data as a copiable markdown text?
  ```

  > Relevant Output: 
        ``` markdown
        # Tomás Solano — InZenFenix  
        **Course:** IIT414W  
        **Date:** 07-03-2026  

        ---

        # System Information
        - OS: CachyOS **6.19.5-3**
        - Python **3.14.3**
        - pip **26.0.1**

        ---

        # Setup Instructions

        ## 1. Open a terminal
        Open **CMD**, **PowerShell**, or **bash** (Linux/macOS).

        ---

        ## 2. Navigate to the project directory
        Move to the folder where the project is located. Example:

        ```bash
        cd C:/Users/[Your_username]/Documents/Github/iit414w-lab00-inzenfenix

        ```

  > Validation: ChatGPT has some issues giving markdowns, since that's the type of format it uses for chatting, however you can make it give you at least some in prompt, after that i checked that what it gave me and what i did as a template was not that different besides improved readability

  > Adaptations: Not much, since I gave it a template to start the prompt I only needed it to improve upon what was already created

  > Final Decision: Partially Used