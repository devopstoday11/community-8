# Kubeflow community calendar

This is location for [Kubeflow community calendar](https://calendar.google.com/calendar/embed?src=kubeflow.org_7l5vnbn8suj2se10sen81d9428@group.calendar.google.com).
You can find list for all meetings in [`calendar.yaml`](calendar.yaml) file.

## Add new meeting to the calendar

To add new meeting to the Kubeflow calendar follow these steps:

1. Add new record to [`calendar.yaml`](calendar.yaml) with meeting parameters.
   Information about each field you can find in the file.

1. After updating the file, you have to ask anyone from [OWNERS](OWNERS) file
   to manually run [`calendar_import.py`](../scripts/calendar_import.py) to update
   Kubeflow calendar.

1. Then you should be able to see your new meeting in the calendar.

## Before running `calendar_import.py`

1. You need to be calendar admin in kubeflow.org.

1. You need to join the [kubeflow-discuss google group](https://groups.google.com/g/kubeflow-discuss), because

    > Tip: If you have "View members" access to a group and create a group event, each member receives an invitation email. If you do not have  “View members” access, the group receives an invitation. Each user must accept the invite for the event to display appear on their calendar.

    Note if you are using a user@kubeflow.org email account, you should join kubeflow-discuss with this account.

1. You need a Google Cloud project (not sure whether it must be in kubeflow.org).

1. Go to https://console.cloud.google.com/apis/credentials, create an OAuth 2.0 Client ID choosing `Desktop app` type.

1. Visit the newly created OAuth 2.0 Client ID and click "Download JSON" button on top.

1. Move the json file to `~/secrest/kf-calendar.oauth_client.json`.

1. `pip install -r scripts/requirements.txt`
