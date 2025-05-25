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
- [src/hello_interface/srv/StringCommand.srv](srv/StringCommand.srv)
- [src/hello_interface/action/StringCommand.action](srv/StringCommand.action)


