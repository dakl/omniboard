# Usage

## Metric Columns

New metric columns can be added to display rolled up metric value (e.g., minimum validation loss, maximum training accuracy, etc.)
To be able to add a metric column, your experiments should track at-least one metric value. 
Check out [sacred documentation](https://sacred.readthedocs.io/en/latest/collected_information.html#metrics-api) for more info.

To add a new Metric Column:
- Click on `+/- Metric Columns` button located on the top right 
of the dashboard
- Click on `+ Add Column` button
- Give a name to the new column, select a metric from the list of options in the dropdown
and select `extrema` for the rollup
- Click `Apply`

![Adding Metrics Columns](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/adding-metrics.png)

Also, check out [How it works](https://vivekratnavel.github.io/omniboard/#/quick-start?id=metric-columns) documentation for more info on how `Metric Columns` are stored in Mongodb.

## Config Columns

Nested configs can be expanded into separate columns by adding new config column
in `Manage Config Columns` dialog.

For instance, if you have the following config
```json
{
    "config": {
      "train" : {
        "batch_size":32,
        "epochs":100,
        "lr":0.01
      }
    }
}
```
Omniboard automatically adds a new column for `train` and displays the whole
object as its value `{"batch_size":32,"epochs":100,"lr":0.01}`. By adding a
new config column, you can expand each of these nested configs into a separate column.

To add a new Config Column:

- Click on Cog/Settings icon located on the top right corner of the dashboard
- Click on `+/- Config Columns`
- Click on `+ Add Column` button
- Give a name to the new column and select a config from the list of options in the dropdown
- Click `Apply`

![Manage Config Columns](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/manage-config-columns.png)

Also, check out [How it works](https://vivekratnavel.github.io/omniboard/#/quick-start?id=config-columns) documentation for more info on how `Config Columns` are stored in Mongodb.

## Download Source Files or Artifacts

To download `Source Files` or `Artifacts`, click on any row of experiment run
and then click on `Source Files` or `Artifacts` from the side menu.

![Source Files Viewer](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/source-file-view.png)

You can then choose to either `Download All` files or `Download` each file individually.

## Change Timezone

All the timestamps are stored in UTC timezone in database and Omniboard 
will try to guess the user timezone and set it as default timezone for 
`start_time`, `stop_time` and `heartbeat` columns. 

To change the default timezone:
- Click the `Cog` icon on the top right corner and select `Settings` from the menu

  ![Settings Menu](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/settings-menu.png)
 
- Select the desired timezone and save the settings

  ![Settings Timezone](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/settings-timezone.png)

## Delete an experiment run

To delete an unwanted experiment run, hover over its `Id` column and click on the delete icon as shown below.

![Delete Run](https://raw.githubusercontent.com/vivekratnavel/omniboard/master/docs/assets/screenshots/delete-run.png)

Click on `Delete` button in the confirmation dialog to delete the run from the database.
