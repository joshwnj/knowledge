# [](#modeling-drafts)modeling drafts

When modeling "drafts" of something (eg. a form with a "save draft" / "resume draft" feature), consider making a _separate model_ altogether for the draft.  Rather than adding a `isDraft` flag to the original model.

## [](#reasons)Reasons

-   validation is different. A draft doesn't need to include required fields, or have intact relationships with linked entities
-   you want to be able to safely save the model without accidentally triggering an action you shouldn't.  Eg. if there's an `afterSave` hook which sends an email, or adds the model to a processing queue, you probably don't want to do that for drafts. Case in point is Bugwolf. There was logic which said _"when a project model is saved, send email invitations to all testers."_
