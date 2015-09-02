# 9xMultiSerial
A simple architecture and tool to operate more multiple serial ports

This is a design create multple tty instance for application space to write and read from the ports.
The user would update a input file similar to the DTS file of linux, with power on default attributes.

The user would also get an interface to change the attributes, based on the parent.

Thus the system would have a parent device that holds data to all the tty device instance.
Each instance shall be for a given tty device, thus an application using the parent can try to access the device of his choice.

parent{
  childs[number of terminals]
  status
  number chidern born
}

childs{
  baudrate
  status
  mode for serial port
  xmit buffer
  xmit len
  rcv buffer
  rcv len
}
