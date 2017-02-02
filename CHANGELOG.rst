=========
CHANGELOG
=========

0.1.10
======

* feature:``TransferManager``: Expose ability to use own executor class for ``TransferManager``


0.1.9
=====

* feature:``TransferFuture``: Add support for setting exceptions on transfer future


0.1.8
=====

* feature:download: Support downloading to FIFOs.


0.1.7
=====

* bugfix:TransferManager: Fix memory leak when using same client to create multiple TransferManagers


0.1.6
=====

* bugfix:download: Fix issue where S3 Object was not downloaded to disk when empty


0.1.5
=====

* bugfix:Cntrl-C: Fix issue of hangs when Cntrl-C happens for many queued transfers
* feature:cancel: Expose messages for cancels


0.1.4
=====

* feature:chunksize: Automatically adjust the chunksize if it doesn't meet S3s requirements.
* bugfix:Download: Add support for downloading to special UNIX file by name


0.1.3
=====

* feature:delete: Add a ``.delete()`` method to the transfer manager.
* bugfix:seekable upload: Fix issue where seeked position of seekable file for a nonmultipart upload was not being taken into account.


0.1.2
=====

* bugfix:download: Patch memory leak related to unnecessarily holding onto futures for downloads.


0.1.1
=====

* bugfix:deadlock: Fix deadlock issue described here: https://bugs.python.org/issue20319 with using concurrent.futures.wait


0.1.0
=====

* feature:copy: Add support for managed copies.
* feature:download: Add support for downloading to a filename, seekable file-like object, and nonseekable file-like object.
* feature:general: Add ``TransferManager`` class. All public functionality for ``s3transfer`` is exposed through this class.
* feature:subscribers: Add subscriber interface. Currently supports on_queued, on_progress, and on_done status changes.
* feature:upload: Add support for uploading a filename, seekable file-like object, and nonseekable file-like object.


0.0.1
=====

* feature:manager: Add boto3 s3 transfer logic to package. (`issue 2 <https://github.com/boto/s3transfer/pull/2>`__)

