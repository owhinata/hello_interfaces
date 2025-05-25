# hello_interfaces

## create package
```bash
ros2 pkg create \
--description "sample of service" \
--license Apache-2.0 \
--destination-directory src \
--build-type ament_cmake \
--dependencies rosidl_default_generators \
--maintainer-email ouwa@emtechs.co.jp \
--maintainer-name KatsumiOuwa \
hello_interfaces
```

## make idl dirctories
```bash
mkdir src/hello_interface/srv src/hello_interface/action
```

## create idl files
- [srv/StringCommand.srv](srv/StringCommand.srv)
- [action/StringCommand.action](action/StringCommand.action)

## modify CMakeLists.txt
https://github.com/owhinata/hello_interfaces/blob/10eb4c45ed359bfa8e3b94bc42f089800d8cf213/CMakeLists.txt#L12-L16

## modify package.xml
https://github.com/owhinata/hello_interfaces/blob/10eb4c45ed359bfa8e3b94bc42f089800d8cf213/package.xml#L12-L14

## build and setup
```bash
colcon build --packages-select hello_interface
. install/setup.bash
```

## check interface
```bash
ros2 interface list
ros2 interface show hello_interfaces/srv/StringCommand
ros2 interface show hello_interfaces/action/StringCommand
```
