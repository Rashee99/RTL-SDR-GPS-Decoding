# RTL-SDR-GPS-Decoding
GPS decoding using RTL-SDR 

# GPS Decoding & Plotting

## 1. Introduction

This document provides a guide on how to receive and decode GPS signals and obtain location coordinates on a map using an RTL-SDR dongle and a GPS antenna.

## 2. Steps

1. **Download GNSS-SDRLIB:**
   - Visit [GNSS-SDRLIB GitHub](https://github.com/taroz/GNSS-SDRLIB).
   - Click on the green "Clone or download" button and select "Download ZIP".
   - Extract the ZIP file into a convenient folder on your PC.

2. **Download RTK-NAVI:**
   - Get the latest version of RTK-NAVI from [RTKLIB website](http://www.rtklib.com/rtklib.htm).
   - Extract the ZIP file into a convenient folder on your PC.

3. **Plug in RTL-SDR:**
   - Connect the RTL-SDR dongle to your PC.

4. **Open GNSS-SDRLIB GUI:**
   - In the GNSS-SDRLIB folder, navigate to the `bin` subfolder.
   - Open `gnss-sdrgui.exe`.

5. **Configure Parameters:**
   - Set the following parameters in the GUI:
     - Change the Input Type to RTL-SDR.
     - Check RTCM MSM and set the Port to 9999.
     - Ensure that "Output Interval" is set to 10Hz.
     - Check "Plot Acquisition" and "Plot Tracking".
     - Optionally enter your approximate latitude and longitude under "MISC" to aid in getting an initial lock.
     - Under GPS, GLONASS, and Galileo headings, ensure that "ALL" is selected.

![Parameters](https://github.com/Rashee99/RTL-SDR-GPS-Decoding/assets/87062307/9fac8acd-a62d-40e5-bcc1-f1ff8041f810)

6. **Start the GNSS-SDRLIB:**

   - Press Start in the GNSS-SDRLIB GUI.
   - A series of command windows will open and close for a few seconds.
   - Afterward, several gnuplot graph windows will open; these can be ignored.

7. **Open RTK-NAVI:**

   - Navigate to the extracted RTK-NAVI folder and enter the bin directory.
   - Open the `rtlnavi.exe` file.

8. **Configure RTK-NAVI:**

   - Click on the "I" button in the upper right region.

9. **Set Rover Configuration:**

   - Place a check mark next to (1) Rover.
   - Change the "Type" to TCP Client and the "Format" to RTCM3.
   - Click on the button with three dots under the leftmost "Opt."
   - Set the "TCP Server Address" to localhost, and the "Port" to 9999.
   - Press the OK button to exit the two windows.

