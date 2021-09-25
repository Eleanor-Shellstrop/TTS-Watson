# Text to Speech with IBM's Watson

This is an exericese to play with Watson, Jupyter Notebook and using Python. 
I followed along a tutorial by Nicholas Renotte on YouTube [found here](https://www.youtube.com/watch?v=8k8S5ruFAUs). I didn't use his exact syntax and instead relied on the Watson API docs [found here](https://cloud.ibm.com/apidocs/text-to-speech?code=python).

Note: I had to turn off my VPN to navigate and create an account on IBM's website. 

## Instructions

### Download libraries and make an IBM Cloud account

If you do not have Python, Jupyter Notebook or an IBM Cloud account:

1. Install Juptyer Notebook or Anaconda
    * [Install Python, or see Anaconda below](https://www.python.org/downloads/)
    * [Install Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/content-quickstart.html)
    * [Install Anaconda, which includes Jupyter Notebook and Python](https://docs.anaconda.com/anaconda/install/index.html)
2. Sign in or Create an IBM account (free tier is fine).
    * [Create account here](https://cloud.ibm.com/registration?target=/catalog/services/discovery?hideTours=true&&cm_sp=WatsonPlatform-WatsonPlatform-_-OnPageNavCTA-IBMWatson_Discovery-_-Watson_Developer_Website)

### Running the Program 
1. Clone the repository
2. On the IBM website, retrieve your API key and URL for the variables in "Authenticate."
    * Find the Text to Speech product and click "Create."
    * Click the "Manage" tab.
    * Copy and paste your API key and URL values in the variables, in single or double quotes. 
    * Do not share your API key with anyone else or upload to any public repository. 

    Note: I had saved my variable to my local environment and used the `.get` method to retrive them.
    If you do not plan to share your repo and want to **only run locally**, you can plug in your variables with the syntax:

    ```python
    url = 'YOUR URL HERE'
    apikey = 'YOUR API KEY HERE'
    ```
3. Open Jupyter Notebook from the command line with `jupyter notebook`. 
4. Open the repository from within Jupyter Notebook.
5. Run all the code cells. 


## Making Changes

Note: Sometimes errors occur when editting linked files (like audio) within the session. You may need to exit out of your Notebook session and close your editor, re-open and run the code cell you changed again.

### Change Text
   
You can make changes to the text and run the program again. The audio files will update with the changes. 

Example: 
Under the `2. Convert a String` synthesize function, you can change the `'Oh hi, Mark'` to any other string. Run the file, reopen your hello_world.wav audio file and listen to the new speech. 

### Change Voice
   
Also, you may change the voice to a different one. Select from the [supported languages and voices](https://cloud.ibm.com/docs/text-to-speech?topic=text-to-speech-voices) list from IBM. 

Example:
Where we have `voice='en-US_AllisonV3Voice'` under `2. Convert a String`, you can change to another English speaker like `'en-US_MichaelV3Voice'`. Run the program again to overwrite your audio files. 

