#
# Makefile
#
# Makefile for macchina.io XBee Sensor Bundle
#

include $(POCO_BASE)/build/rules/global

include $(POCO_BASE)/OSP/BundleCreator/BundleCreator.make

INCLUDE += -I$(PROJECT_BASE)/devices/Devices/include
INCLUDE += -I$(PROJECT_BASE)/protocols/XBee/include

objects = XBeeSensor BundleActivator

target         = io.macchina.xbee.sensor
target_version = 1
target_libs    = IoTXBee IoTDevices PocoRemotingNG PocoOSP PocoUtil PocoXML PocoFoundation

postbuild      = $(SET_LD_LIBRARY_PATH) $(BUNDLE_TOOL) -n$(OSNAME) -a$(OSARCH) -o../bundles XBeeSensor.bndlspec

include $(POCO_BASE)/build/rules/dylib
