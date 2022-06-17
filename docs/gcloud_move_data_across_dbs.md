#### Transfer Data From One Database To Another on GCloud

* In Dashboard, navigate to SQL -> `instance`
* To export data,
   * click `export`
   * choose `file format`
   * optional: offload data to temporary instance so you can do other things while it loads in the bg.
   * choose database from `instance` to export.
   * select a `storage location` to export into.
   * export

* To import it, click `import`, fill the necessary fields and import from `storage location`.

* To scan with Data Loss Prevention,
   * Navigate to `storage location`, click on actions and choose scan with DLP

* To delete,
   * Navigate to `storage location`, click on actions and delete.