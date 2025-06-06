# Usage Guide

This guide describes how to configure and run the Edeal Metadata Cleaner application.

## Launching the application

1. Install the project dependencies with `npm install` if you haven't already.
2. Execute `npx electron .` from the project root to open the desktop interface.

## Cleaning a file

1. Click **Sélectionner un fichier** or drag an XML file onto the window.
2. Press **Nettoyer** to start the process. A progress bar will show the current percentage.
3. You can stop the cleaning at any time using the stop icon next to the progress bar.
4. The cleaned file is produced next to the original with the extension `.new`.

## Configuring radicals

1. Choose **Options > Paramètres** from the menu.
2. Enter one or more radicals separated by `;` and click **Ajouter**.
3. Radicals appear in a list where you can remove them.
4. Click **Sauvegarder** to persist them to the settings file or **Annuler** to discard changes.

The settings are stored in `APPDATA/settings.raw` so they are reused the next time you start the program.

