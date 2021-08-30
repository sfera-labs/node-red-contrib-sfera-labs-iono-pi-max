# Iono Pi Max Node-RED

Node-RED for Iono Pi Max - the industrial Raspberry Pi PLC.

Install and run Node-RED on Iono Pi Max and access all its functionalities with this module.

## Setup

Before using this node make sure the [Iono Pi Max kernel module](https://github.com/sfera-labs/iono-pi-max-kernel-module) is installed on Iono Pi Max.

## Usage

This node lets you control and monitor the functionalities of Iono Pi Max
by reading/writing the sysfs files provided by its
<a href="https://github.com/sfera-labs/iono-pi-max-kernel-module" target="_blank">Kernel module</a>.


### Inputs
<dl class="message-properties">
    <dt>payload - <span class="property-type">string | number</span></dt>
    <dd>the value to write or empty to only trigger a read.</dd>
</dl>

### Outputs
<dl class="message-properties">
  (Readable features only)
  <dt>payload - <span class="property-type">string</span></dt>
  <dd>the value read.</dd>
</dl>

In the configuration, select the functionality (sysfs file) to link this node to.
Functionalities can be readable (R) and/or writable (W).<br>
Use <code>msg.payload</code> as the value to write to or read from the file.

For details on the values' formats refer to the
<a href="https://github.com/sfera-labs/iono-pi-max-kernel-module#readme" target="_blank">Kernel module documentation</a>.
