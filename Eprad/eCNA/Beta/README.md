# Eprad eCNA Plugin

Version: 1.3

Author: Steve Guttag

## Description

The Eprad eCNA plugin is designed to aid in the integration of the Eprad eCNA line of cinema automations. Key features include:

- **I/O Flag Control/Monitor**: Provides full monitoring over the Input and Output flags as well control over the Output flags. 
- **Macro Execution**: Provides for direct execution of any of the eCNA's Macros.
- **RDI Execution**: Provides for the execution of any of the RDI (Remote Devices) command execution.
- **Program Control and Monitoring**: The eCNA can run a traditional cinema automation program (step through a program one cue at a time).
- **Eprad Dimmer Monitoring and Control**: As of version 1.2, the plugin can now monitor and control an Eprad QDC-400 type dimmer.
- **Eprad nanoHost Monitoring**: As of version 1.3, the plugin can now monitor the Eprad nanoHost.

## Pages

The plugin contains up to eight pages:

1. **Setup**: Enter IP address and desired port (defaults to 13002).  The Model and firmware version number is retrieved.
2. **Outputs**: Output Flag status and Control.  Aux Output Names are fetched from the eCNA.
3. **Dimmer Control**: Option (configured in Properties) to monitor/control Eprad QDC-400 series dimmers. 
4. **Inputs**: Input Flag Status.  Aux Input Flag Names are fetched from the eCNA.
5. **Macros**: Macro Execution Trigger Buttons.
6. **RDI**: RDI Execution Trigger Buttons.
7. **Program**: eCNA Program control and Mmonitoring.
8. **NanoHost**: Option(Configured in Properties) to monitor the Eprad nanoHost (show schedules).  

## Properties

- **NumMacros**: The number of macros you want to be available (0-50).
- **NumRDI**: The number of remote devices (RDI) you want to be available. 
- **ScrapeInterval**: The rate that Input and Output flags are updated (0.5-20 seconds; 2-second default).  Times below 1.3-seconds will cause a slow-down of the the eCNA's web-ui.
- **LightPollInterval**: New for 1.2.  Sets the rate at which the dimmer controls are polled for status (0.5 - 20 seconds; 3-second default).
- **EnableQDC_Lighting**: When set to Yes (default is No) the Dimmer Control Tab is revealed.
- **QDCZones**: Set the number of lighting Zones (1-16) for the QDC-400 dimmer (default is 2; House and Stage).
- **QDCChannels**: Set the number of QDC-400 dimmer channels (1-16) (default is 2). 
- **EnableNanoHost**: When set to YEs (default is No) the NanoHost tab is revealed. 
- **Show Debug**:  Standard Q-SYS Debug window.

## Usage

1. Drag the plugin into your design.
2. Enter the IP of the target device and the Desired Port (13002 by default)
3. The plugin should populate and get the current status, at that point.  If it doesn't you may be using a port already occupied. 
4. Drag out any desired buttons or LEDs that suit your design. The Aux buttons were deliberately not named to allow for integrator naming. 
5. Expose the desired Input/Output pins to integrate the automation within a Q-SYS design.
6. Configure Eprad QDC-400 dimmer properties to mach the installed dimmer.  

## What's New in 1.3

- Added Eprad Nano Host monitoring.
- Screen number is fetched on the Setup Page.

## Images 

<img width="684" height="727" alt="image" src="https://github.com/user-attachments/assets/e97caee6-153a-4cae-a98b-ed633a57f97e" />

<img width="799" height="933" alt="image" src="https://github.com/user-attachments/assets/0442da97-67ad-49a4-bf51-d21919a54859" />

<img width="830" height="536" alt="image" src="https://github.com/user-attachments/assets/8a90502b-27dc-452f-a1f0-1d5764b592cf" />

<img width="680" height="605" alt="image" src="https://github.com/user-attachments/assets/1971cd37-6e6b-485b-846b-3b0409da31ab" />

<img width="686" height="377" alt="image" src="https://github.com/user-attachments/assets/30f1c185-70d3-472f-9145-68a21ffcabac" />

<img width="683" height="783" alt="image" src="https://github.com/user-attachments/assets/b7c7d56e-e040-4a32-ac64-2267b376068c" />

<img width="683" height="557" alt="image" src="https://github.com/user-attachments/assets/764cb9cc-0ce7-462e-bc67-39cc0f794242" />

<img width="761" height="809" alt="image" src="https://github.com/user-attachments/assets/70fdd42a-3731-4ab7-a533-65cfa8cd43bb" />



## Requirements

- Q-SYS Designer 9.0 or higher (Primary development was on 9.13.1 LTS and checked on 9.4.8 LTS and 10.4.0)
- Q-SYS Core devices

## Support

This software is being supplied as-is and without support.  However, you may request support or changes to the author.  Please see the standard MIT License and Help File for more details.  
