### Set dark mode on chrome
```bash
sudo sed -i 's/^Exec=\/usr\/bin\/google-chrome-stable$/& --enable-features=WebUIDarkMode --force-dark-mode/' /usr/share/applications/google-chrome.desktop

sudo sed -i 's/%U/--enable-features=WebUIDarkMode --force-dark-mode &/' /usr/share/applications/google-chrome.desktop                      
```