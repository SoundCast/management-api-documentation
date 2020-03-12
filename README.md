# management-api-documentation

SoundCast provides an API to manage networks, sites, tags as well as getting reporting on campaigns.

In this repository, you will find indications on how to use that API as well as a YAML that you can read with any openapi v2.0 YAML reader.

To use this API you need a SoundCast user account. If you don't have an account yet, contact the SoundCast team.

## Authentication

To authenticate, use the `/user/auth` path to get a JWT token.

## Reporting

SoundCast provides a path to get reports on campaign. As openapi has its limitation, we will cover some of the subtilities of this path.

The reports show values only when an impression or completion has been made.

The `/report` path has a `group_by` query parameter to add dimension to the result.

You can find the supported values in the table below.

| value | description |
| ----- | ----------- |
| campaignId | add the campaigns |
| adId | add the ads |
| country | add the country |
| region | add the region |
| department | add department |
| city | add city |
| keywords | add keywords |
| month | add month |
| week | add weeks |
| day | add day |
| hour | add hours |
| networkId | add networks |
| siteId | add sites |
| tagId | add tags |
