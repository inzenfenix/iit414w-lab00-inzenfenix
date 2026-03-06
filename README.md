# Tomás Solano, InZenFenix, IIT414W, 07-03-2026
 
## System Info
    - CachyOS Version 6.19.5-3
    - Python 3.14.3
    - pip 26.0.1

## Setup Instructions
1. Open CMD, Powershell or bash (if using linux)
2. Choose the directory of this folder, for example:
    ``` bash
    cd C:/Users/[Your_username]/Documents/Github/iit414w-lab00-inzenfenix
    ```
3. Run the following command to create a python environment, add a dot to it to hide it from git:
    ``` bash
        python -m venv .venv

        If that doesn't work try:

        python3 -m venv .venv
    ```

4. Next We'll start the virtual environment:
    ``` bash
        source .venv/bin/activate

        Some Operative Systems use different files to start, for example CachyOS uses:

        source .venv/bin/activate.fish

        And powershell uses:

        source .venv/bin/activate.ps1
    ```

5. Once inside the virtual environment, we can add the needed libraries:
    ``` bash
        pip install -r requirements.txt
    ```

6. To start the Notebooks, you can run the jupyter lab:
    ``` bash
        jupyter lab
    ```
    
    - Once that's done It will open the lab automatically with the notebook if It doesn't you can check for yourself with:
        > It will give you a bunch of lines, check for the one that looks like:
        ``` bash
            [I 2026-03-06 20:23:26.043 ServerApp] http://localhost:8888/lab?token=6bdadd316fe5eb2941e8797c93d90e4233a49ba6e3c82dc0
        ```
    > It creates a page which you can copy and paste to your favorite browser where You'll be capable of running the notebook.