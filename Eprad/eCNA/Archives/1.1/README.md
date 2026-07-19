# Eprad eCNA Plugin

Version: 1.1.2

Author: Steve Guttag

## Description

The Eprad eCNA plugin is designed to aid in the integration of the Eprad eCNA line of cinema automations. Key features include:

- **I/O Flag Control/Monitor**: Provides full monitoring over the Input and Output flags as well control over the Output flags. 
- **Macro Execution**: Provides for direct execution of any of the eCNA's Macros.
- **RDI Execution**: Provides for the execution of any of the RDI (Remote Devices) command execution.
- **Program Control and Monitoring**: The eCNA can run a traditional cinema automation program (step through a program one cue at a time).

## Pages

The plugin contains six pages:

1. **Setup**: Enter IP address and desired port (defaults to 13002).  The Model and firmware version number is retrieved.
2. **Outputs**: Output Flag status and Control.  Aux Output Names are fetched from the eCNA. 
3. **Inputs**: Input Flag Status.  Aux Input Flag Names are fetched from the eCNA.
4. **Macros**: Macro Execution Trigger Buttons.
5. **RDI**: RDI Execution Trigger Buttons.
6. **Program**: eCNA Program control and Mmonitoring. 

## Properties

- **NumMacros**: The number of macros you want to be available (0-50).
- **NumRDI**: The number of remote devices (RDI) you want to be available. 
- **PollRate**: The speed of refresh of non-Input/Output status (1-60 seconds; default 30) Mostly a safety since the plugin also receives this information via an automatic update from the eCNA upon a change in state.  
- **ScrapeRate**: The rate that Input and Output flags are updated (1-60 seconds; 3-second default).  Times below 2-seconds will cause a slow-down of the the eCNA's web-ui.  
- **Auto Refresh Names**: The plugin will fetch the Aux Input and Aux Output names.  However, if the integrator changes one of those names, the plugin will only (automatically) update if this setting is set to yes (default = Yes).

## Usage

1. Drag the plugin into your design.
2. Enter the IP of the target device and the Desired Port (13002 by default)
3. The plugin should populate and get the current status, at that point.  If it doesn't you may be using a port already occupied. 
4. Drag out any desired buttons or LEDs that suit your design. The Aux buttons were deliberately not named to allow for integrator naming. 
5. Expose the desired Input/Output pins to integrate the automation within a Q-SYS design.   

## Images

<img width="687" height="619" alt="image" src="https://github.com/user-attachments/assets/5c01b97f-06fb-496b-8cb0-0236e2436b91" />

<img width="686" height="932" alt="image" src="https://github.com/user-attachments/assets/6457bb32-30ff-4113-9b68-921ce96d2cdf" />

<img width="682" height="663" alt="image" src="https://github.com/user-attachments/assets/771efff6-e3c5-4fb0-bbee-e1f300b6b562" />

<img width="686" height="377" alt="image" src="https://github.com/user-attachments/assets/30f1c185-70d3-472f-9145-68a21ffcabac" />

<img width="683" height="783" alt="image" src="https://github.com/user-attachments/assets/b7c7d56e-e040-4a32-ac64-2267b376068c" />

<img width="683" height="557" alt="image" src="https://github.com/user-attachments/assets/764cb9cc-0ce7-462e-bc67-39cc0f794242" />

## Requirements

- Q-SYS Designer 9.0 or higher (Primary development was on 9.13.1 LTS and checked on 9.4.8 LTS and 10.4.0)
- Q-SYS Core devices

## Support

This software is being supplied as-is and without support.  However, you may request support or changes to the author.  Please see the standard MIT License and Help File for more details.  
