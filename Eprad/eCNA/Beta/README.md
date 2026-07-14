# Eprad eCNA Plugin

Version: 1.2

Author: Steve Guttag

## Description

The Eprad eCNA plugin is designed to aid in the integration of the Eprad eCNA line of cinema automations. Key features include:

- **I/O Flag Control/Monitor**: Provides full monitoring over the Input and Output flags as well control over the Output flags. 
- **Macro Execution**: Provides for direct execution of any of the eCNA's Macros.
- **RDI Execution**: Provides for the execution of any of the RDI (Remote Devices) command execution.
- **Program Control and Monitoring**: The eCNA can run a traditional cinema automation program (step through a program one cue at a time).

## Pages

The plugin contains upto sevem pages:

1. **Setup**: Enter IP address and desired port (defaults to 13002).  The Model and firmware version number is retrieved.
2. **Outputs**: Output Flag status and Control.  Aux Output Names are fetched from the eCNA.
3. **Dimmer Control**: Option (configured in Properties) to monitor/control Eprad QDC-400 series dimmers. 
4. **Inputs**: Input Flag Status.  Aux Input Flag Names are fetched from the eCNA.
5. **Macros**: Macro Execution Trigger Buttons.
6. **RDI**: RDI Execution Trigger Buttons.
7. **Program**: eCNA Program control and Mmonitoring. 

## Properties

- **NumMacros**: The number of macros you want to be available (0-50).
- **NumRDI**: The number of remote devices (RDI) you want to be available. 
- **ScrapeInterval**: The rate that Input and Output flags are updated (0.5-20 seconds; 2-second default).  Times below 1.3-seconds will cause a slow-down of the the eCNA's web-ui.
- **LightPollInterval**: New for 1.2.  Sets the rate at which the dimmer controls are polled for status (0.5 - 20 seconds; 3-second default).
- **EnableQDC_Lighting**: When set to Yes (default is No) the Dimmer Control Tab is revealed.
- **QDCZones**: Set the number of lighting Zones (1-16) for the QDC-400 dimmer (default is 2; House and Stage).
- **QDCChannels**: Set the number of QDC-400 dimmer channels (1-16) (default is 2). 
- **Auto Refresh Names**: The plugin will fetch the Aux Input and Aux Output names.  However, if the integrator changes one of those names, the plugin will only (automatically) update if this setting is set to yes (default = Yes).
- **Show Debug**:  Standard Q-SYS Debug window.

## Usage

1. Drag the plugin into your design.
2. Enter the IP of the target device and the Desired Port (13002 by default)
3. The plugin should populate and get the current status, at that point.  If it doesn't you may be using a port already occupied. 
4. Drag out any desired buttons or LEDs that suit your design. The Aux buttons were deliberately not named to allow for integrator naming. 
5. Expose the desired Input/Output pins to integrate the automation within a Q-SYS design.
6. Configure Eprad QDC-400 dimmer properties to mach the installed dimmer.  

## What's New in 1.2

Version 1.2 adds optional monitoring and control of Eprad QDC-400 dimmer lighting boards, replicating the eCNA's own Status: Light Control web page, plus several changes to existing behavior:

- **QDC-400 Dimmer Lighting** — new optional Dimmer Control page with per-zone preset buttons (Up/Down/Mid1/Mid2/None), an offset fader with dedicated increase/decrease step buttons, and animated per-channel level meters. See QDC-400 Dimmer Lighting.
- Scrape Interval — accepts fractional seconds (e.g. 1.6), not just whole seconds. See Properties.
- Light Poll Interval — new property controlling how often dimmer status is polled, independently of Scrape Interval. See Light Poll Interval.
- Faster Digital Projector status — the four Digital Projector Power/Video buttons now update immediately from the eCNA's own unsolicited event reports rather than waiting on the next scrape. See Digital Projectors.
- Poll Rate removed — no longer a configurable property; the plugin now uses a fixed 45-second rate.
- Auto Refresh Names removed — input/output names (and, when dimmer lighting is enabled, zone names and QDC board detection) are now fetched once on connect and otherwise only on demand. See Refresh Setup Data.
- Refresh buttons consolidated — the separate Refresh Input Names / Refresh Output Names buttons have been replaced by a single Refresh Setup Data button on the Setup page.
- Debug tab removed — the Show Debug Tab property, its Debug page, and the Last_Tx/Last_Rx/Last_Error pins are gone; everything they showed is already in the Q-SYS Debug window. See Show Debug Tab under Properties if you had anything wired to those specific pins.

## Images 

<img width="684" height="727" alt="image" src="https://github.com/user-attachments/assets/e97caee6-153a-4cae-a98b-ed633a57f97e" />

<img width="686" height="930" alt="image" src="https://github.com/user-attachments/assets/c4b9e5bd-4575-4497-9761-f2186dfeb8c5" />

<img width="830" height="536" alt="image" src="https://github.com/user-attachments/assets/8a90502b-27dc-452f-a1f0-1d5764b592cf" />

<img width="680" height="605" alt="image" src="https://github.com/user-attachments/assets/1971cd37-6e6b-485b-846b-3b0409da31ab" />

<img width="686" height="377" alt="image" src="https://github.com/user-attachments/assets/30f1c185-70d3-472f-9145-68a21ffcabac" />

<img width="683" height="783" alt="image" src="https://github.com/user-attachments/assets/b7c7d56e-e040-4a32-ac64-2267b376068c" />

<img width="683" height="557" alt="image" src="https://github.com/user-attachments/assets/764cb9cc-0ce7-462e-bc67-39cc0f794242" />

Copyright ©2026 by Steven Guttag

This Component may be distributed freely.  Use at your own risk. 

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

Any changes by others may be appended but under no circumstances may the 
original copyright be removed. 

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
