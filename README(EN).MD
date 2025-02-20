# Piper Robotic Arm SDK Demo

[中文](README.MD)

![ubuntu](https://img.shields.io/badge/Ubuntu-20.04-orange.svg)

Test:

|PYTHON |STATE|
|---|---|
|![python3.8](https://img.shields.io/badge/Python-3.8-blue.svg)|![Pass](https://img.shields.io/badge/Pass-blue.svg)|

## Installation Instructions

### Install Dependencies

```shell
pip3 install python-can
```

```shell
pip3 install piper_sdk
```

For CAN module activation, refer to [can README](./can_config.MD)

## Demo Explanation

```shell
├── V1
│   ├── can_config.MD
│   ├── interface_disconnect.py
│   ├── motor_max_acc_limit_config.py
│   ├── piper_disable.py
│   ├── piper_enable.py
│   ├── piper_end_pose.py
│   ├── piper_gripper_ctrl.py
│   ├── piper_gripper_zero_set.py
│   ├── piper_init_default.py
│   ├── piper_joint_ctrl.py
│   ├── piper_master_config.py
│   ├── piper_moveC.py
│   ├── piper_multi_interface_instance.py
│   ├── piper_read_arm_motor_max_acc_limit.py
│   ├── piper_read_arm_motor_max_angle_spd.py
│   ├── piper_read_end_pose.py
│   ├── piper_read_fk.py
│   ├── piper_read_high_msg.py
│   ├── piper_read_slow_msg.py
│   ├── piper_reset.py
│   ├── piper_set_mit.py
│   ├── piper_slave_config.py
│   ├── piper_status.py
│   ├── piper_stop.py
│   ├── read_all_fps.py
│   ├── read_gripper_status.py
│   ├── read_joint_state.py
│   ├── README(EN).MD
│   ├── README.MD
│   └── read_piper_hardware.py
└── V2
    ├── can_config.MD
    ├── interface_disconnect.py
    ├── motor_max_acc_limit_config.py
    ├── piper_disable.py
    ├── piper_enable.py
    ├── piper_end_pose.py
    ├── piper_gripper_ctrl.py
    ├── piper_gripper_zero_set.py
    ├── piper_init_default.py
    ├── piper_joint_ctrl.py
    ├── piper_master_config.py
    ├── piper_moveC.py
    ├── piper_multi_interface_instance.py
    ├── piper_read_arm_motor_max_acc_limit.py
    ├── piper_read_arm_motor_max_angle_spd.py
    ├── piper_read_end_pose.py
    ├── piper_read_fk.py
    ├── piper_read_high_msg.py
    ├── piper_read_slow_msg.py
    ├── piper_reset.py
    ├── piper_set_mit.py
    ├── piper_slave_config.py
    ├── piper_status.py
    ├── piper_stop.py
    ├── read_all_fps.py
    ├── read_gripper_status.py
    ├── read_joint_state.py
    ├── README(EN).MD
    ├── README.MD
    ├── read_piper_hardware.py
    ├── V2_gripper_param_config.py
    ├── V2_installation_pos.py
    ├── V2_joint_mit_ctrl.py
    └── V2_motor_max_spd_set.py
```

|File |Description|
|---|---|
|`motor_max_acc_limit_config.py`|Sets the maximum acceleration limit for a specific joint motor|
|`piper_disable.py`|Disables the robotic arm|
|`piper_enable.py`|Enables the robotic arm|
|`piper_end_pose.py`|Controls the robotic arm's end pose|
|`piper_gripper_ctrl.py`|Controls the robotic arm's gripper|
|`piper_gripper_zero_set.py`|Sets the gripper to its zero position|
|`piper_init_default.py`|Sets all joint limits, joint max speed, and joint acceleration to default values|
|`piper_joint_ctrl.py`|Controls the robotic arm's joints|
|`piper_master_config.py`|Sets the robotic arm to master arm mode|
|`piper_moveC.py`|Sets the robotic arm to master arm mode|
|`piper_read_arm_motor_max_acc_limit.py`|Reads the maximum acceleration limits for all motors|
|`piper_read_arm_motor_max_angle_spd.py`|Reads the maximum speed limits for all motors of the robotic arm|
|`piper_read_end_pose.py`|Reads the end pose of the robotic arm|
|`piper_reset.py`|Resets the robotic arm; must be done after setting to teaching mode|
|`piper_set_mit.py`|Sets the robotic arm to MIT mode, for faster response|
|`piper_slave_config.py`|Sets the robotic arm to slave arm mode|
|`piper_status.py`|Reads the robotic arm's status|
|`piper_stop.py`|Stops the robotic arm's slow fall; needs reset and re-enable twice after use|
|`read_gripper_status.py`|Reads the gripper status|
|`read_joint_state.py`|Reads and prints joint angle messages|
|`read_piper_hardware.py`|Reads the robotic arm's main controller firmware version|
|`V2_gripper_param_config.py`|V2 version of the gripper parameter settings|
|`V2_installation_pos.py`|V2 version for setting the installation position to horizontal|
|`V2_joint_mit_ctrl.py`|V2 version for setting individual motor MIT parameters|
|`V2_motor_max_spd_set.py`|V2 version for setting the maximum speed limit of a specific joint motor|

Note: If the robotic arm is in master arm mode, after sending the command to switch to slave arm mode, a reboot is required for the arm to switch to slave arm mode.