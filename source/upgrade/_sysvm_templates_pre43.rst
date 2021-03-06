.. Licensed to the Apache Software Foundation (ASF) under one
   or more contributor license agreements.  See the NOTICE file
   distributed with this work for additional information#
   regarding copyright ownership.  The ASF licenses this file
   to you under the Apache License, Version 2.0 (the
   "License"); you may not use this file except in compliance
   with the License.  You may obtain a copy of the License at
   http://www.apache.org/licenses/LICENSE-2.0
   Unless required by applicable law or agreed to in writing,
   software distributed under the License is distributed on an
   "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
   KIND, either express or implied.  See the License for the
   specific language governing permissions and limitations
   under the License.

.. sub-section included in upgrade notes.

Update System-VM templates
--------------------------

.. note::
   Upgrading pre-4.3 to 4.4.1 require 2 systemvm templates downloaded: the 4.3 and 4.4.

#. While running the existing |version_to_upgrade| system, log in to the UI as 
   root administrator.

#. In the left navigation bar, click Templates.

#. In Select view, click Templates.

#. Register 4.3 systemvm template:
   
   #. Click Register template.

      The Register template dialog box is displayed.

   #. In the Register template dialog box, specify the following values
      (do not change these):
   
      +------------+------------------------------------------------------------+
      | Hypervisor | Description                                                |
      +============+============================================================+
      | XenServer  | Name: systemvm-xenserver-4.3                               |
      |            |                                                            |
      |            | Description: systemvm-xenserver-4.3                        |
      |            |                                                            |
      |            | URL: |acs43-sysvm64-url-xen|                               |
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: XenServer                                      |
      |            |                                                            |
      |            | Format: VHD                                                |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+
      | KVM        | Name: systemvm-kvm-4.3                                     |
      |            |                                                            |
      |            | Description: systemvm-kvm-4.3                              |
      |            |                                                            |
      |            | URL: |acs43-sysvm64-url-kvm|                               |  
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: KVM                                            |
      |            |                                                            |
      |            | Format: QCOW2                                              |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+
      | VMware     | Name: systemvm-vmware-4.3                                  |
      |            |                                                            |
      |            | Description: systemvm-vmware-4.3                           |
      |            |                                                            |
      |            | URL: |acs43-sysvm64-url-vmware|                            |
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: VMware                                         |
      |            |                                                            |
      |            | Format: OVA                                                |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+

#. Register |version| systemvm template:
   
   #. Click Register template.

      The Register template dialog box is displayed.

   #. In the Register template dialog box, specify the following values
      (do not change these):
      
      +------------+------------------------------------------------------------+
      | Hypervisor | Description                                                |
      +============+============================================================+
      | XenServer  | Name: systemvm-xenserver-|version|                         |
      |            |                                                            |
      |            | Description: systemvm-xenserver-|version|                  |
      |            |                                                            |
      |            | URL: |sysvm64-url-xen|                                     |
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: XenServer                                      |
      |            |                                                            |
      |            | Format: VHD                                                |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+
      | KVM        | Name: systemvm-kvm-|version|                               |
      |            |                                                            |
      |            | Description: systemvm-kvm-|version|                        |
      |            |                                                            |
      |            | URL: |sysvm64-url-kvm|                                     |  
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: KVM                                            |
      |            |                                                            |
      |            | Format: QCOW2                                              |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+
      | VMware     | Name: systemvm-vmware-|version|                            |
      |            |                                                            |
      |            | Description: systemvm-vmware-|version|                     |
      |            |                                                            |
      |            | URL: |sysvm64-url-vmware|                                  |
      |            |                                                            |
      |            | Zone: Choose the zone where this hypervisor is used        |
      |            |                                                            |
      |            | Hypervisor: VMware                                         |
      |            |                                                            |
      |            | Format: OVA                                                |
      |            |                                                            |
      |            | OS Type: Debian GNU/Linux 7.0 (64-bit) (or the             |
      |            | highest Debian release number available in the             |
      |            | dropdown)                                                  |
      |            |                                                            |
      |            | Extractable: no                                            |
      |            |                                                            |
      |            | Password Enabled: no                                       |
      |            |                                                            |
      |            | Public: no                                                 |
      |            |                                                            |
      |            | Featured: no                                               |
      |            |                                                            |
      |            | Routing: no                                                |
      +------------+------------------------------------------------------------+

#. Watch the screen to be sure that the template downloads successfully and 
   enters the **READY** state. Do not proceed until this is successful.
