# How to Boot into CLI Only and Use GUI Temporarily on Linux

Follow these steps to set your system to boot into the command-line interface (CLI) only by default, with the option to start and stop the graphical user interface (GUI) as needed.

---

## Step 1: Set the system to boot into CLI only by default

Run this command once to set the default target to multi-user (text mode):

```bash
sudo systemctl set-default multi-user.target
```

---

## Step 2: Start the GUI temporarily when needed

From your CLI session, run the following command to start the graphical desktop environment for the current session:

```bash
sudo systemctl start graphical.target
```

This will launch the GUI without changing the default boot mode.

---

## Step 3: Stop the GUI and return to CLI

When you’re done with the GUI and want to return to the CLI prompt, stop the graphical interface by running:

```bash
sudo systemctl stop graphical.target
```

You will be returned to the CLI (TTY).