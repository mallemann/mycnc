# Disclaimer

This repository documents a private hobby project. It is published **as-is** for inspiration and personal experiments. It is not a commercial product, has not been certified, and has not been tested for any purpose other than my own use.

## No warranty, no liability

- All information, drawings, bills of materials, parameters and links are provided **without any warranty** of any kind, express or implied, including accuracy, completeness or fitness for a particular purpose.
- To the extent permitted by law, the author accepts **no liability** for any damage, injury, loss or cost resulting from the use of this information, from building a machine based on it, or from operating such a machine.
- **You build and operate anything based on this repository entirely at your own risk.** You are responsible for complying with the safety regulations and laws that apply where you live.

## Safety notes

- **Mains voltage:** The control cabinet, power supplies and spindle drives work with mains voltage. Wiring must be done by a qualified person. Make sure the cabinet is properly earthed, fused and closed.
- **Emergency stop:** The emergency-stop chain must **really cut the power** to the drives and the spindle. A software signal to the controller is not enough.
- **Spindle and moving axes:** A running spindle and moving axes can cause severe injuries. Never reach into the working area while the machine is running. Wear eye protection and hearing protection, secure workpieces and tools properly.
- **Dust and chips:** Wood dust and chips can be harmful and flammable. Use extraction and keep the machine clean.
- **Test first:** Check new programs in a simulation first, then run them above the workpiece without cutting – especially for 4- and 5-axis jobs.
- **Adapt the parameters:** Motor currents, microstepping, steps per mm or degree, limit-switch logic, homing, feed rates and accelerations must match **your** mechanics and electronics. The values in this repository come from my build and are not meant to be copied blindly.

## Licenses

The disclaimers of warranty and limitations of liability in [LICENSE](LICENSE) (CERN-OHL-S-2.0) and [LICENSE-docs](LICENSE-docs) (CC BY-SA 4.0) apply in addition.
