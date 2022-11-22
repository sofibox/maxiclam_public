Maxiclam Documentation

Maxiclam is a bash script CLI extension that can manage both ClamAV antivirus and
Linux Malware Detect (maldet) with extra features.
Visit ClamAV official website at: https://www.clamav.net/ and visit Linux Malware Detect (maldet) official
website at: https://www.rfxn.com/projects/linux-malware-detect/

Script Author: Arafat Ali | Email: arafat@sofibox.com | (C) 2019-2022

Usage:

maxiclam <-SHORT_OPTIONS/--LONG_OPTIONS>
maxiclam <ACTIONS> <-SHORT_OPTIONS/--LONG_OPTIONS>

example:

# use clamav
maxiclam scanx --path /var/www/html
# use maldet
maxiaide scan --path /var/www/html

OPTIONS:

  -h, --help, help, /?, ?
        This is a help text.

  -v, -V, --version, version, ver
        Show version information

  -t, --test
        A placeholder for a unit test

ACTIONS:

  scan, maldet

        Run system scan using clamav

        OPTIONAL PARAMETER(S):

          -j, --cron, --cronjob
          Run the scan in cronjob mode

          -p, --path, --scan-path
          Provide the starting file/path to scan

          -e, --email
          Enable email report. Even if this option is present, it will not send email if there is no warning appear
          from the scan. Please make sure that the email report format is valid or the script will prompt to correct it

  scanx, clamav

        Run system scan using clamav

        OPTIONAL PARAMETER(S):

          -j, --cron, --cronjob
          Run the scan in cronjob mode

          -p, --path, --scan-path
          Provide the starting file/path to scan

          -e, --email
          Enable email report. Even if this option is present, it will not send email if there is no warning appear
          from the scan. Please make sure that the email report format is valid or the script will prompt to correct it

          -v, --verbose
          Run the scan in verbose mode

          -d, --debug
          Run the scan in debug mode

          -q, --quite
          Run the scan in quite mode
          Note that when this option is present, it will ignore both -v and -d options

          -i, --infected, show-infected-only
          Only show infected file and ignore other warnings


  file-list, list-file

      OPTIONAL PARAMETER(S):
          --edit, --edit-maldet
          This will open up a text editor to edit maldet list of ignored file/path from scanning

          --edit-clamav
          This will open up a text editor to edit clamav list of ignored file from scanning

          --clear, --clear-maldet
          This will clear maldet list of ignored file/path from scanning

          --clear-clamav
          This will clear clamav list of ignored file from scanning

          --view, --show, --view-maldet, --show-maldet
          This will display maldet list of ignored file/path from scanning

          --view-clamav, --show-clamav
          This will display clamav list of ignored file from scanning


  dir-list, list-dir, directory-list, list-directory

      OPTIONAL PARAMETER(S):
          --edit, --edit-maldet
          This will open up a text editor to edit maldet list of ignored file/path from scanning

          --edit-clamav
          This will open up a text editor to edit clamav list of ignored directory from scanning

          --clear, --clear-maldet
          This will clear maldet list of ignored file/path from scanning

          --clear-clamav
          This will clear clamav list of ignored directory from scanning

          --view, --show, --view-maldet, --show-maldet
          This will display maldet list of ignored file/path from scanning

          --view-clamav, --show-clamav
          This will display clamav list of ignored directory from scanning



  ext-list, list-ext, extension-list, list-extension

      OPTIONAL PARAMETER(S):
          --edit, --edit-maldet
          This will open up a text editor to edit maldet list of ignored extension from scanning

          --edit-clamav
          This will open up a text editor to edit clamav list of ignored extension from scanning

          --clear, --clear-maldet
          This will clear maldet list of ignored extension from scanning

          --clear-clamav
          This will clear clamav list of ignored extension from scanning

          --view, --show, --view-maldet, --show-maldet
          This will display maldet list of ignored extension from scanning

          --view-clamav, --show-clamav
          This will display clamav list of ignored extension from scanning


  sign-list, list-sign, signature-list, list-signature

      OPTIONAL PARAMETER(S):
          --edit, --edit-maldet
          This will open up a text editor to edit maldet list of ignored signature from scanning

          --edit-clamav
          This will open up a text editor to edit clamav list of ignored signature from scanning

          --clear, --clear-maldet
          This will clear maldet list of ignored signature from scanning

          --clear-clamav
          This will clear clamav list of ignored signature from scanning

          --view, --show, --view-maldet, --show-maldet
          This will display maldet list of ignored signature from scanning

          --view-clamav, --show-clamav
          This will display clamav list of ignored signature from scanning


  inot-list, list-inot, inotify-list, list-inotify
     This action only available for maldet

     OPTIONAL PARAMETER(S):
         --edit, --edit-maldet
         This will open up a text editor to edit maldet list of ignored inotify from scanning

         --clear, --clear-maldet
         This will clear maldet list of ignored inotify from scanning

         --view, --show, --view-maldet, --show-maldet
         This will display maldet list of ignored inotify from scanning

  update

      Update both clamav database signature and maldet version and signature

  init

      Initialize clamav and maldet config and exclusion rules

  clearlog, removelog, cleanlog

       Clean old logs except the latest log

  latestlog, lastlog, lastreport

       Read the latest generated report