**Simple CLI LLM Chat**
======================

Simple CLI Python script to interact with commercial or self-hosted LLMs using the LiteLLM library.

Started this script as a self-educational project but found it so useful that now it has turned into my AI daily-driver.

**Features**
------------

* Supports as much LLM providers as [LiteLLM supports](https://litellm.vercel.app/docs/)
* Configure your own servers as default servers
* Automatic chat backup to a file
* Interactive and non-interactive modes
* Code block extraction in non-interactive mode
* Customizable prompt style

**Usage**
---------

### Interactive Mode

1. Run the script without sending any text via stdin.
2. Type a message and press Enter to receive a response from the AI.
3. Press Ctrl+C to exit.

### Non-Interactive Mode

1. Pipe a message to the script using `echo "message" | python ai.py`.
2. The script will process the message and print the response.
3. Use the `-s` or `--strip` option to extract only code blocks from the response.
* `-h` or `--help`: Display usage information.
* `-l` or `--light`: Use a light theme for the prompt.
* `-s` or `--strip`: Extract only code blocks from the response in non-interactive mode.
* `-m` or `--model`: Define the target LLM model.

To see how you must define the model look in the [LiteLLM documentation](https://litellm.vercel.app/docs/providers), API keys must be defined using environment variables as described there.

**Configuration**
---------------

* The script uses the `PROVIDERS` list to configure the default LLM providers. Is a good place to configure your own server(s).
* The `BACKUP` variable specifies the file path for automatic chat backup.

**Requirements**
---------------

* Python 3.x
* LiteLLM library
* requests library
* prompt_toolkit library

**License**
-------

This script is released under the MIT License. See LICENSE.txt for details.
