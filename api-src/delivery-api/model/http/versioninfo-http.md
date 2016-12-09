# VersionInfo

## Overview

This object contains all the information relating to the versioning information for an entry or asset. The *created* and *createdBy* property values are established on the creation of the resource and do not change, whereas the remaining property values change as the resource is either modified or published.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| created | string | The date the entry was created |
| createdBy | string | The user id of who created the entry |
| modified | string | The date the entry version was last modified |
| modifiedBy | string | The user id of who last modified the entry |
| published | string | The date the entry version was last published |
| publishedBy | string | The user id of who last published the entry |
| versionNo | string | The version of the entry | 

## Remarks

The *versionNo* follows a two-part versioning scheme:

> {Major}.{Minor}

The *minor* part is incremented on every sucessful update to the entry. The *major* part is incremented once the entry has been approved and subsequently published which in turn resets the {minor} part to zero.