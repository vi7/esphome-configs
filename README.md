ESPHome configurations
======================

Usage
-----

Install and activate Python3 virtualenv:
```bash
pip3 install virtualenv
python3 -m virtualenv venv
source venv/bin/activate
```

Install required Python packages (**virtualenv must be activated!**, see above):
```bash
pip install -r requirements.txt
```

Copy [secrets.yaml.example](./secrets.yaml.example) file to `secrets.yaml` (will be ignored by Git) and populate with required secrets.

For the first time firmware upload physically connect board to the computer via USB cable, all subsequent uploads could be performed as OTA updates.

Compile and upload ESPHome configuration. Example for the BLE gateway config:
```bash
esphome run radio-gateway.yaml
```

`run` command will automatically compile firmware, upload it to the board and then attach board log output to the terminal.
