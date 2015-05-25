.. Project-FiFo documentation master file, created by
   Heinz N. Gies on Fri Aug 15 03:25:49 2014.

********
Machines
********

List
####

.. image:: /_static/images/jingles/machines01.png

The **Machines** tab is the central area within the UI where new virtual machines are created and where most of the actions related to existing virtual machines are performed.

1. The filter entry area |filter entry area| is designed to selectively filter the machines that are displayed in your list by your filter criteria. The filter is designed to remember the criteria you have filtered by and will continue filtering by those criteria even if you leave and return to the machines tab.

.. |filter entry area| image:: /_static/images/jingles/machines03.png

2. Clicking on the |new machine button| will launch a new UI page which contains options relevant to new VM creation.

.. |new machine button| image:: /_static/images/jingles/machines04.png

3. The **Action Icons** are used to perform specific actions on machines directly from list view list.

  1. |button 1| Launch zone/kvm console.
  2. |button 2| Power on a machine.

  .. |button 1| image:: /_static/images/jingles/machines-kvm.png
  .. |button 2| image:: /_static/images/jingles/machines-zone.png

____

Create
######

.. image:: /_static/images/jingles/machines05.png

1. Choose the name or alias of your new machine.
2. Choose the dataset that will be used for your new machine.
3. Choose the package that will be used for your new machine.
4. Choose the network/s your machine will be connected to.

   .. hint::

      You will only be able to select more than 1 network if the package selected supports multiple networks.

5. Choose optional advanced parameters if you require them.

.. image:: /_static/images/jingles/machines06.png

6. Click the |create button| button to start machine creation.

.. |create button| image:: /_static/images/jingles/create.png

____

Details
#######

.. image:: /_static/images/jingles/machines07.png

1. Shows the current real-time state of the machine.

2. These **Action Buttons** perform the following actions:

 - |button destroy|     Destroy the machine (can only be selected if machine is both *stopped* and *not lock protected*)
 - |button console|     Launch the machine's zone or kvm console.
 - |button lock|        Lock protect the machine to ensure no accidental changes can be made.
 - |button start|       Start the machine, only clickable if machine is in a stopped state.
 - |button restart|     Restart the machine, only clickable if machine is in a running state.
 - |button stop|        Stop the machine, only clickable if machine is in a running state.

.. |button destroy| image:: /_static/images/jingles/machines-destroy.png
.. |button console| image:: /_static/images/jingles/machines-console.png
.. |button lock| image:: /_static/images/jingles/machines-lock.png
.. |button start| image:: /_static/images/jingles/machines-start.png
.. |button restart| image:: /_static/images/jingles/machines-restart.png
.. |button stop| image:: /_static/images/jingles/machines-stop.png

3. Machine sub tabs contain sub sections relevant to your machine, we will explore each one in more detail below.
4. Sub tab display area will show you information related to the sub tab you have selected.
5. The default "details" tab includes a color selector which will mark your VM a certain color in the "machine list" view page. This is useful for easily and quickly identifying certain machines in the list or for grouping certain types of machines by colors.
6. Clicking on the |button configuration| configuration icon will expand a section which will allow you to change certain machine fields.

.. |button configuration| image::  /_static/images/jingles/machines-configuration.png

____

|picture|

 - **Describe**: An internal own use field that can be enabled as one of the columns in machine list view.
 - **Alias**: Change the alias of the machine.
 - **Hostname**: Change the hostname of the machine.
 - **Resolvers**: Change the resolvers of the machine.
 - **Owner**: Change the owner of the machine.

.. |picture| image:: /_static/images/jingles/machines-conf.png

____

.. todo::

  Sections for the other subtabs need to be added.

Machine Performance TAB
***********************

.. image:: /_static/images/jingles/machines08.png

The **Performance** tab shows various metrics and performance graphs relating to the machine:

- Disk IOPS
- Disk throughput
- Memory usage
- Swap Usage
- CPU usage
- Network throughput
- Network packets per second

Snapshots
*********

.. image:: /_static/images/jingles/machines09.png

The **Snapshots** tab lets you create snapshots and roll back to previous snapshots. The rollback icon will only be visible if the machine is in a *stopped* state and is not *lock protected*.  To create a snapshot simply click the |snapshot button| button and enter a name/comment for your snapshot in the snapshot popup window. Click the |ok button| button to create the machine.

.. |snapshot button| image:: /_static/images/jingles/machines-snapshot.png
.. |ok button| image:: /_static/images/jingles/machines-snapshot-ok.png

.. Attention::
    When rolling back to a snapshot all snapshots that were created after the rollback date will be destroyed. To delete a specific snapshot click on the |trash| icon next to the snapshot.

.. |trash| image:: /_static/images/jingles/machines-destroy.png


Resize
******

.. image:: /_static/images/jingles/machines10.png

The **Resize** tab is used to upgrade or downgrade your VM by associating it with a different package. The CPU share, CPU cap, ram and disk size will be changed when a package is changed. To do this simply select a new package in the **Change to** area and select an option in the |selection panel| selection panel. Than press the |change button| to apply the change. The change will be applied in real time if the machine is a smartmachine / zone based machine. If the machine is KVM based it will require a shutdown and startup for the changes to take effect.

.. |selection panel| image:: /_static/images/jingles/machines-selection.png
.. |change button| image:: /_static/images/jingles/machines-change.png


History
*******

.. image:: /_static/images/jingles/machines11.png

In the **History** tab you can view a chronological record or log of any actions or changes performed on that machine. All entries are associated with a date/time entry related to when the change occurred.


Notes
*****

.. image:: /_static/images/jingles/machines12.png

In the **Note** tab you to record notes or details related to the machine. This can be any information that you deem useful and would like to remember. To create a note simply click on the **+** button and type your note into the popup dialogue and then click ok to create the note. Each individual note is time stamped so you know when it was created. To delete a note, simply click on the |delete note button| icon in the top right hand corner of the note.

.. |delete note button| image:: /_static/images/jingles/machines-notes-destroy.png
