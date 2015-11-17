The GO bind utilizes work from pyangbind

Pre-requesitis are Python 2.7 and pyang 1.6 (may work with other version but work was tested against these versions)

to execute here is an example:
cd ~/git/external/src/github.com/openconfig/release/models/bgp
// pick a file to run against I chose openconfig-bgp.yang 
pyang ~/git/external/src/github.com/pyangbind/gobind/ -f pybind openconfig-bgp.yang -o test.go	

code expects the -o test.go and it will convert it to fmt_test.go. 

11/13/15 - Created initial structs, New method, and Set method for each member of the struct.  This is initial code generation and has not been tested.

11/17/15 - File name inputed does not matter, a new file will be generated with prefix of fmt_xxxx
Union and leaf-lists have been flattened out for purposes of being able to use the structs generated in a db fashion.

code was run against openconfig interface
pyang --plugindir ~/git/external/src/github.com/pyangbind/gobind -f pybind -o if.go *.yang



