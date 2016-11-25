# VersionInfo

## Overview

This type contains all the information relating to the versioning information for an entry or asset. The *Created* and *CreatedBy* property values are established on the creation of the resource and do not change, whereas the remaining property values change as the resource is either modified or published.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| Created | DateTime | The date the entry was created |
| CreatedBy | string | The user id of who created the entry |
| Modified | DateTime | The date the entry version was last modified |
| ModifiedBy | string | The user id of who last modified the entry |
| Published | DateTime | The date the entry version was last published |
| PublishedBy | string | The user id of who last published the entry |
| VersionNo | string | The version of the entry | 

## Remarks

The *VersionNo* follows a two-part versioning scheme:

> {Major}.{Minor}

The *minor* part is incremented on every sucessful update to the entry. The *major* part is incremented once the entry has been approved and subsequently published, which in turn resets the *minor* part to zero.