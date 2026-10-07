This repository contains figures and raw data related to the ICTSS2026 paper "Conexa: Online Conformance and Exhibition-Driven Model-Based Testing".

For the preprint version of the paper, [Conexa preprint pdf](https://github.com/S-van-den-Broek-UvA/MBT_DSP/blob/master/Conexa_ICTSS2026/Conexa%20preprint%20[contains%20minor%20mistakes%20in%20examples%3B%20will%20be%20fixed%20in%20Springer%20version].pdf). Note that this preprint version contains two minor mistakes in examples/figures, which will be fixed in the official print version by Springer. These changes do not influence the results presented in the paper in any way.

Repository contents:
- STS model of the SmartDoor SUT
- STS models of all test purposes created for the SmartDoor
- Raw data (test case steps) of Conexa x all test purposes
- Raw data (test case steps) of the random strategy
- Raw data (test case steps) of the transition coverage strategy

The table below shows all of SmartDoor's behavioral requirements and their descriptions. A test purpose was modeled for each of these.

| Requirement | Description |
| --- | --- |
| BEHAVR-01 | When the door is closed and unlocked, it may be opened. |
| BEHAVR-02 | When the door is opened, it may be closed. |
| BEHAVR-03 | When the door is closed and unlocked, it may be locked. |
| BEHAVR-04 | When the door is closed and locked, it may be unlocked. |
| BEHAVR-05 | All other commands must be refused. |
| SECLOC-03 | When the lock command is used with a valid passcode, the door can only be unlocked with an unlock command containing that exact passcode. Other passcodes are considered incorrect. |
| SECLOC-04 | When the lock command is used with an invalid passcode, the command must be refused and then door must return the invalid_passcode response. |
| SECLOC-05 | When the unlock command is used with an incorrect passcode, the command must be refused and the door must return the incorrect_passcode response. |
| SECLOC-06 | When the unlock command is used with an invalid passcode, the command must be refused and the door must return the invalid_passcode response. |
| SECLOC-07 | When the unlock command is used three times with an incorrect passcode, the door must shut off and not respond to any commands until it is restarted physically. |
