### 2021-11-09 (Build 20211109-005902.15cf6819)
- **[FEAT]** You can now view all of the environment variables that were captured when the process was started.

  ![Environment variables in metadata dropdown](https://static.metawork.com/images/metadata_env_vars.png)
  
  Simply click on the `ENV` value chip to see all of the variables and their values.

- **[FEAT]** Search results have been moved to a dropdown similar to the metadata change made in the last release.

  ![Search results dropdown](https://static.metawork.com/images/search_results_dropdown.png)

- **[PERF]** On large datasets, seach queries will now run _much_ faster (an order of magnitude faster, in some cases).
- **[BUG]** We fixed an error that occurred in Ruby when an ActiveJob was spawned outside of instrumented code.
- **[BUG]** We fixed a regression in the `upload-logs` CLI command that prevented uploads.
- **[MISC]** We switched to stream-oriented processing of recording frames in the Metawork service.

  This will enable the viewing of "in-flight" recordings in the future. This way, users will be able to watch long-running recordings live in the UI as new frames come in (the work to support this in the UI is still pending, however).

### 2021-10-29 (Build 20211029-172859.e16aa2ab)
- **[BUG]** We fixed a backwards-incompatible data change that resulted in old recordings failing to load.

### 2021-10-29 (Build 20211029-091740.107e4267)
- **[FEAT]** We've added a panel where you can view useful metadata about your recording.

  ![Metadata dropdown](https://static.metawork.com/images/metadata_dropdown.png)
  
  Let us know if there are other pieces of information you'd like see here!
  
- **[LANG]** The following language versions have been removed and will be automatically updated:
  | Old | New |
  | --- | --- |
  | Ruby 2.7.3 | Ruby 2.7.4 |
  | Node 16.11.1 | Node 16.13.0 |
  
  Our policy is to be fairly aggressive with language updates during the alpha, but would appreciate feedback on cadence.
- **[MISC]** We removed the automatic waitlist for new users
  
  We think the software has stabilized enough that we can remove this obstacle to getting started for new users.
