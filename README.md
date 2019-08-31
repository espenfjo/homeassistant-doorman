# homeassistant-doorman
Custom component for the Yale Doorman lock(s) via the Yale Smart HUB.

Supports:
 * Reading current state
 * Reading past state via the report API (Same as the history in the app)

Unsupported:
* Unlocking or locking the door (Although trivial to implement)
  * Endpoint for unlocking is: /yapi/api/minigw/unlock/
    * Parameters for unlocking (YMMV): area=1&zone=1&pincode=xxxxxxxx
  * Endpoint for locking is: /yapi/api/panel/device_control/
    * Parameters for locking: area=1&zone=1&device_sid=RF%3Axxxxxxxx&device_type=device_type.door_lock&request_value=1 (`device_id` is feteched from `device_status[0]['device_id']`)

Tested with the V2N lock.

## Installation

Place the `custom_components` folder in your Home Assistant configuration folder.

See https://developers.home-assistant.io/docs/en/creating_component_loading.html for more information

