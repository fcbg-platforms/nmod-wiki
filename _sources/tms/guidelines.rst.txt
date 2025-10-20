.. include:: ../links.inc

Guidelines (TMS)
================

Motor threshold
---------------

For TMS, the intensity of pulses is set as a percentage of the individual
:term:`motor threshold`. The individual :term:`motor threshold` varies greatly
inter-subject, but also intra-subject between separate sessions. Thus, the individual
:term:`motor threshold` should **always** be re-estimated at the beginning of each
session.

To prevent any risk for the participant, repetitive TMS is usually capped at 70 to 80%
of the individual :term:`motor threshold` and single pulse TMS is usually capped at 120%
of the individual :term:`motor threshold`.

Magstim devices
---------------

The Magstim devices share common features: similar interface design, similar
:term:`coil` design, similar connector design.

.. tab-set::

    .. tab-item:: Interface

        The interface has 3 buttons, green, yellow, and red, used to control the
        stimulation pulses, and one nob used to set the stimulation settings.

        - The green button is used to *charge* the devices.
        - The yellow button is used to *deliver* a single pulse.
        - The red button is used to *discharge* the devices.

        .. attention::

            The Magstim devices should always be discharged before:

            - plugging/unplugging a :term:`coil`
            - shutting down the device

        .. image:: ../_static/magstim/magstim-buttons.png
            :align: center
            :class: img-with-border
            :width: 50%

    .. tab-item:: Coil connector

        .. attention::

            When plugging or unplugging a :term:`coil`, extreme care should be taken to
            avoid bending the pins.

        When plugging the connector, position it as straight as possible, insert it
        gently in the correct orientation and tigheten the ring by turning it clockwise.

        When unplugging the connector, untightened the ring by turning it
        counter-clockwise, support the connector cable with one hand to avoid any stress
        on the pins and pull the connector as straight as possible.

        .. image:: ../_static/magstim/magstim-connector.png
            :align: center
            :class: img-with-border
            :width: 50%

    .. tab-item:: Delivering a pulse

        Pulse delviery can be controlled either by triggers, by pressing the yellow
        button on the interface or by pressing the connected pedal (if available). In
        anycase, the pulse will not be delivered if the button on the :term:`coil`
        handle is not pressed simultaneously.

        .. tip::

            This safety features can be disabled by blocking the button on the handle of
            the :term:`coil` in-place with a ziptie. Responsibilities for any damage or
            injury caused by this modification are on the user.

        .. image:: ../_static/magstim/magstim-safety.png
            :align: center
            :width: 50%

        The pulse will not be delivered if the :term:`coil` is overheating. In this
        case, please let the :term:`coil` cool down before trying again.

        .. tip::

            Discharge the stimulator and replace the :term:`coil` with a fresh one if
            needed.

        Pulse delivery yields an audible click, which gets louder as the pulse intensity
        is increased.

        .. attention::

            If possible, avoid delivering pulses with the :term:`coil` next to the
            stimulator or next to electronic devices, as it could damage them.

Piloting a TMS study
--------------------

For piloting purposes, an osciloscope can be used to measure the stimulation pulses via
a 3-coil probe, measuring directly the magnetic field. The probe should be attached in
the center of the :term:`TMS coil`.
