# New laptop setup
> Checklist Template https://github.com/scoremedia/automation-guide/blob/master/doc/New_Laptop_Setup.md

## Checklist:

- [ ] 1. Install your preferred IDE : most of us are using IntelliJ IDEA and also sometimes Visual Studio Code
- [ ] 2. Install Google Chrome browser (useful for day to day but also required by our Selenium driver)
- [ ] 3. Ensure the shell is set to bash: `chsh -s /bin/bash`
- [ ] 4. Remove the preinstalled JRE:
    ```
    # https://stackoverflow.com/questions/64917779/wrong-java-home-after-upgrade-to-macos-big-sur-v11-0-1
    sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
    sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefpane
    ```
- [ ] 5. Install Xcode from the App Store and run it at least once.
    - [ ] Install Xcode command line tools: `xcode-select --install`
- [ ] 6. Allow installing packages from brew: `sudo spctl --master-disable`
- [ ] 7. Enable MacOS developer mode:`sudo DevToolsSecurity -enable`
- [ ] 8. Install [homebrew](https://brew.sh/).
- [ ] 9. [Generate new ssh keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for github access.
- [ ] 10. Clone [automation-ci](https://github.com/scoremedia/automation-ci) repo and run [setup_env.sh](https://github.com/scoremedia/automation-ci/blob/master/scripts/setup_env.sh).
    - [ ] Address any errors and actionable messages from the `setup_env.sh` output.
- [ ] 11. Restart laptop and ensure `appium-doctor` returns no blocking errors.

**After running through the setup steps you may need to tweak a few things, most solutions can be found by googling the error messages and/or asking the team for help.**
