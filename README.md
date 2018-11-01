# dismantle-pulseaudio
Force-disable PulseAudio

The following is tested and working on Fedora 29, and should work on other operating systems that use systemd:

```BASH
git clone https://github.com/Markieta/dismantle-pulseaudio.git
sudo cp dismantle-pulseaudio/dismantle-pulseaudio.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now dismantle-pulseaudio.service
```

This will now rename the `pulseaudio` binary to `pulseaudio.bak`, preventing its unsolicited execution.
