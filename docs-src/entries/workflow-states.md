# Workflow states
Entries exist in a workflow state. They have one of the following states, Draft, Awaiting publish or Published. If a multi lingual license is present then the Awaiting translation and Not yet translated states come in to use.

## Draft
When an entry is created it is in the draft state until it has been published for the first time.

A **Draft** entry is indicated in a listing with a grey border or has a grey lozenge in the entry editor. 

Another indication that the item is in draft is that it has no major version in its version number *e.g.* 0.6.

## Awaiting publish
When an entry has been published at least once, and has had changes made to it and saved. Then the entry is placed into the Awaiting publish state until it is published.

It's effectively published and has a new draft state. 

An entry marked as **Awaiting publish** is indicated in a listing with an orange border or has a orange lozenge in the entry editor. 

Another indication that the item is in the Awaiting publish state is that it has major and minor number in its version number *e.g.* 1.6.

## Published
When an entry is published and has had no further changes made to it. The entry will be in the published state.

An entry marked as **Published** is indicated in a listing with a green border or has a green lozenge in the builder. 

Another indication that the item is in the Published state is that it only has a major number in its version number *e.g.* 2.0.

## Not yet translated *(licensed feature)*
When a language variation exists and its content has not yet been created then the entry will have the Not yet translated state.

## Awaiting translation *(licensed feature)*
When a language variation has a published version and changes to the master language have been made then the entry will have the Awaiting translation state.