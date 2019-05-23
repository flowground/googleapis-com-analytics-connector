# ![LOGO](logo.png) Google Analytics **flow**ground Connector

## Description

A generated **flow**ground connector for the Google Analytics API (version v3).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/analytics/v3/swagger.json<br/>
Generated at: 2019-05-23T12:12:56+03:00

## API Description

Views and manages your Google Analytics data.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Returns Analytics data for a view (profile).

*Tags:* `data`

#### Input Parameters
* `dimensions` - _optional_ - A comma-separated list of Analytics dimensions. E.g., 'ga:browser,ga:city'.
* `end-date` - _required_ - End date for fetching Analytics data. Request can should specify an end date formatted as YYYY-MM-DD, or as a relative date (e.g., today, yesterday, or 7daysAgo). The default value is yesterday.
* `filters` - _optional_ - A comma-separated list of dimension or metric filters to be applied to Analytics data.
* `ids` - _required_ - Unique table ID for retrieving Analytics data. Table ID is of the form ga:XXXX, where XXXX is the Analytics view (profile) ID.
* `include-empty-rows` - _optional_ - The response will include empty rows if this parameter is set to true, the default is true
* `max-results` - _optional_ - The maximum number of entries to include in this feed.
* `metrics` - _required_ - A comma-separated list of Analytics metrics. E.g., 'ga:sessions,ga:pageviews'. At least one metric must be specified.
* `output` - _optional_ - The selected format for the response. Default format is JSON.
    Possible values: dataTable, json.
* `samplingLevel` - _optional_ - The desired sampling level.
    Possible values: DEFAULT, FASTER, HIGHER_PRECISION.
* `segment` - _optional_ - An Analytics segment to be applied to data.
* `sort` - _optional_ - A comma-separated list of dimensions or metrics that determine the sort order for Analytics data.
* `start-date` - _required_ - Start date for fetching Analytics data. Requests can specify a start date formatted as YYYY-MM-DD, or as a relative date (e.g., today, yesterday, or 7daysAgo). The default value is 7daysAgo.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.

### Returns Analytics Multi-Channel Funnels data for a view (profile).

*Tags:* `data`

#### Input Parameters
* `dimensions` - _optional_ - A comma-separated list of Multi-Channel Funnels dimensions. E.g., 'mcf:source,mcf:medium'.
* `end-date` - _required_ - End date for fetching Analytics data. Requests can specify a start date formatted as YYYY-MM-DD, or as a relative date (e.g., today, yesterday, or 7daysAgo). The default value is 7daysAgo.
* `filters` - _optional_ - A comma-separated list of dimension or metric filters to be applied to the Analytics data.
* `ids` - _required_ - Unique table ID for retrieving Analytics data. Table ID is of the form ga:XXXX, where XXXX is the Analytics view (profile) ID.
* `max-results` - _optional_ - The maximum number of entries to include in this feed.
* `metrics` - _required_ - A comma-separated list of Multi-Channel Funnels metrics. E.g., 'mcf:totalConversions,mcf:totalConversionValue'. At least one metric must be specified.
* `samplingLevel` - _optional_ - The desired sampling level.
    Possible values: DEFAULT, FASTER, HIGHER_PRECISION.
* `sort` - _optional_ - A comma-separated list of dimensions or metrics that determine the sort order for the Analytics data.
* `start-date` - _required_ - Start date for fetching Analytics data. Requests can specify a start date formatted as YYYY-MM-DD, or as a relative date (e.g., today, yesterday, or 7daysAgo). The default value is 7daysAgo.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.

### Returns real time data for a view (profile).

*Tags:* `data`

#### Input Parameters
* `dimensions` - _optional_ - A comma-separated list of real time dimensions. E.g., 'rt:medium,rt:city'.
* `filters` - _optional_ - A comma-separated list of dimension or metric filters to be applied to real time data.
* `ids` - _required_ - Unique table ID for retrieving real time data. Table ID is of the form ga:XXXX, where XXXX is the Analytics view (profile) ID.
* `max-results` - _optional_ - The maximum number of entries to include in this feed.
* `metrics` - _required_ - A comma-separated list of real time metrics. E.g., 'rt:activeUsers'. At least one metric must be specified.
* `sort` - _optional_ - A comma-separated list of dimensions or metrics that determine the sort order for real time data.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists account summaries (lightweight tree comprised of accounts/properties/profiles) to which the user has access.

*Tags:* `management`

#### Input Parameters
* `max-results` - _optional_ - The maximum number of account summaries to include in this response, where the largest acceptable value is 1000.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists all accounts to which the user has access.

*Tags:* `management`

#### Input Parameters
* `max-results` - _optional_ - The maximum number of accounts to include in this response.
* `start-index` - _optional_ - An index of the first account to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists account-user links for a given account.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve the user links for.
* `max-results` - _optional_ - The maximum number of account-user links to include in this response.
* `start-index` - _optional_ - An index of the first account-user link to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Adds a new user to the given account.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the user link for.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Removes a user from the given account.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the user link for.
* `linkId` - _required_ - Link ID to delete the user link for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates permissions for an existing user on the given account.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to update the account-user link for.
* `linkId` - _required_ - Link ID to update the account-user link for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists all filters for an account

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve filters for.
* `max-results` - _optional_ - The maximum number of filters to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new filter.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create filter for.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Delete a filter.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the filter for.
* `filterId` - _required_ - ID of the filter to be deleted.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Returns a filters to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve filters for.
* `filterId` - _required_ - Filter ID to retrieve filters for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing filter. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the filter belongs.
* `filterId` - _required_ - ID of the filter to be updated.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing filter.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the filter belongs.
* `filterId` - _required_ - ID of the filter to be updated.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists web properties to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve web properties for. Can either be a specific account ID or '~all', which refers to all the accounts that user has access to.
* `max-results` - _optional_ - The maximum number of web properties to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new property if the account has fewer than 20 properties. Web properties are visible in the Google Analytics interface only if they have at least one profile.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the web property for.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Gets a web property to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve the web property for.
* `webPropertyId` - _required_ - ID to retrieve the web property for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing web property. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the web property belongs
* `webPropertyId` - _required_ - Web property ID
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the web property belongs
* `webPropertyId` - _required_ - Web property ID
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### List custom data sources to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account Id for the custom data sources to retrieve.
* `max-results` - _optional_ - The maximum number of custom data sources to include in this response.
* `start-index` - _optional_ - A 1-based index of the first custom data source to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property Id for the custom data sources to retrieve.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Delete data associated with a previous upload.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account Id for the uploads to be deleted.
* `customDataSourceId` - _required_ - Custom data source Id for the uploads to be deleted.
* `webPropertyId` - _required_ - Web property Id for the uploads to be deleted.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### List uploads to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account Id for the uploads to retrieve.
* `customDataSourceId` - _required_ - Custom data source Id for uploads to retrieve.
* `max-results` - _optional_ - The maximum number of uploads to include in this response.
* `start-index` - _optional_ - A 1-based index of the first upload to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property Id for the uploads to retrieve.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Upload data for a custom data source.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account Id associated with the upload.
* `customDataSourceId` - _required_ - Custom data source Id to which the data being uploaded belongs.
* `webPropertyId` - _required_ - Web property UA-string associated with the upload.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### List uploads to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account Id for the upload to retrieve.
* `customDataSourceId` - _required_ - Custom data source Id for upload to retrieve.
* `uploadId` - _required_ - Upload Id to retrieve.
* `webPropertyId` - _required_ - Web property Id for the upload to retrieve.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists custom dimensions to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom dimensions to retrieve.
* `max-results` - _optional_ - The maximum number of custom dimensions to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID for the custom dimensions to retrieve.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new custom dimension.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom dimension to create.
* `webPropertyId` - _required_ - Web property ID for the custom dimension to create.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Get a custom dimension to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom dimension to retrieve.
* `customDimensionId` - _required_ - The ID of the custom dimension to retrieve.
* `webPropertyId` - _required_ - Web property ID for the custom dimension to retrieve.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing custom dimension. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom dimension to update.
* `customDimensionId` - _required_ - Custom dimension ID for the custom dimension to update.
* `ignoreCustomDataSourceLinks` - _optional_ - Force the update and ignore any warnings related to the custom dimension being linked to a custom data source / data set.
* `webPropertyId` - _required_ - Web property ID for the custom dimension to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing custom dimension.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom dimension to update.
* `customDimensionId` - _required_ - Custom dimension ID for the custom dimension to update.
* `ignoreCustomDataSourceLinks` - _optional_ - Force the update and ignore any warnings related to the custom dimension being linked to a custom data source / data set.
* `webPropertyId` - _required_ - Web property ID for the custom dimension to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists custom metrics to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom metrics to retrieve.
* `max-results` - _optional_ - The maximum number of custom metrics to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID for the custom metrics to retrieve.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new custom metric.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom metric to create.
* `webPropertyId` - _required_ - Web property ID for the custom dimension to create.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Get a custom metric to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom metric to retrieve.
* `customMetricId` - _required_ - The ID of the custom metric to retrieve.
* `webPropertyId` - _required_ - Web property ID for the custom metric to retrieve.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing custom metric. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom metric to update.
* `customMetricId` - _required_ - Custom metric ID for the custom metric to update.
* `ignoreCustomDataSourceLinks` - _optional_ - Force the update and ignore any warnings related to the custom metric being linked to a custom data source / data set.
* `webPropertyId` - _required_ - Web property ID for the custom metric to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing custom metric.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the custom metric to update.
* `customMetricId` - _required_ - Custom metric ID for the custom metric to update.
* `ignoreCustomDataSourceLinks` - _optional_ - Force the update and ignore any warnings related to the custom metric being linked to a custom data source / data set.
* `webPropertyId` - _required_ - Web property ID for the custom metric to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists webProperty-Google Ads links for a given web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the account which the given web property belongs to.
* `max-results` - _optional_ - The maximum number of webProperty-Google Ads links to include in this response.
* `start-index` - _optional_ - An index of the first webProperty-Google Ads link to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID to retrieve the Google Ads links for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Creates a webProperty-Google Ads link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the Google Analytics account to create the link for.
* `webPropertyId` - _required_ - Web property ID to create the link for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Deletes a web property-Google Ads link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the account which the given web property belongs to.
* `webPropertyAdWordsLinkId` - _required_ - Web property Google Ads link ID.
* `webPropertyId` - _required_ - Web property ID to delete the Google Ads link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Returns a web property-Google Ads link to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the account which the given web property belongs to.
* `webPropertyAdWordsLinkId` - _required_ - Web property-Google Ads link ID.
* `webPropertyId` - _required_ - Web property ID to retrieve the Google Ads link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing webProperty-Google Ads link. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the account which the given web property belongs to.
* `webPropertyAdWordsLinkId` - _required_ - Web property-Google Ads link ID.
* `webPropertyId` - _required_ - Web property ID to retrieve the Google Ads link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing webProperty-Google Ads link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - ID of the account which the given web property belongs to.
* `webPropertyAdWordsLinkId` - _required_ - Web property-Google Ads link ID.
* `webPropertyId` - _required_ - Web property ID to retrieve the Google Ads link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists webProperty-user links for a given web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID which the given web property belongs to.
* `max-results` - _optional_ - The maximum number of webProperty-user Links to include in this response.
* `start-index` - _optional_ - An index of the first webProperty-user link to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web Property ID for the webProperty-user links to retrieve. Can either be a specific web property ID or '~all', which refers to all the web properties that user has access to.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Adds a new user to the given web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the user link for.
* `webPropertyId` - _required_ - Web Property ID to create the user link for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Removes a user from the given web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the user link for.
* `linkId` - _required_ - Link ID to delete the user link for.
* `webPropertyId` - _required_ - Web Property ID to delete the user link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates permissions for an existing user on the given web property.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to update the account-user link for.
* `linkId` - _required_ - Link ID to update the account-user link for.
* `webPropertyId` - _required_ - Web property ID to update the account-user link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists views (profiles) to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID for the view (profiles) to retrieve. Can either be a specific account ID or '~all', which refers to all the accounts to which the user has access.
* `max-results` - _optional_ - The maximum number of views (profiles) to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID for the views (profiles) to retrieve. Can either be a specific web property ID or '~all', which refers to all the web properties to which the user has access.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the view (profile) for.
* `webPropertyId` - _required_ - Web property ID to create the view (profile) for.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Deletes a view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the view (profile) for.
* `profileId` - _required_ - ID of the view (profile) to be deleted.
* `webPropertyId` - _required_ - Web property ID to delete the view (profile) for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Gets a view (profile) to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve the view (profile) for.
* `profileId` - _required_ - View (Profile) ID to retrieve the view (profile) for.
* `webPropertyId` - _required_ - Web property ID to retrieve the view (profile) for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing view (profile). This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the view (profile) belongs
* `profileId` - _required_ - ID of the view (profile) to be updated.
* `webPropertyId` - _required_ - Web property ID to which the view (profile) belongs
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the view (profile) belongs
* `profileId` - _required_ - ID of the view (profile) to be updated.
* `webPropertyId` - _required_ - Web property ID to which the view (profile) belongs
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists profile-user links for a given view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID which the given view (profile) belongs to.
* `max-results` - _optional_ - The maximum number of profile-user links to include in this response.
* `profileId` - _required_ - View (Profile) ID to retrieve the profile-user links for. Can either be a specific profile ID or '~all', which refers to all the profiles that user has access to.
* `start-index` - _optional_ - An index of the first profile-user link to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web Property ID which the given view (profile) belongs to. Can either be a specific web property ID or '~all', which refers to all the web properties that user has access to.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Adds a new user to the given view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the user link for.
* `profileId` - _required_ - View (Profile) ID to create the user link for.
* `webPropertyId` - _required_ - Web Property ID to create the user link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Removes a user from the given view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the user link for.
* `linkId` - _required_ - Link ID to delete the user link for.
* `profileId` - _required_ - View (Profile) ID to delete the user link for.
* `webPropertyId` - _required_ - Web Property ID to delete the user link for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates permissions for an existing user on the given view (profile).

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to update the user link for.
* `linkId` - _required_ - Link ID to update the user link for.
* `profileId` - _required_ - View (Profile ID) to update the user link for.
* `webPropertyId` - _required_ - Web Property ID to update the user link for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists experiments to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve experiments for.
* `max-results` - _optional_ - The maximum number of experiments to include in this response.
* `profileId` - _required_ - View (Profile) ID to retrieve experiments for.
* `start-index` - _optional_ - An index of the first experiment to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID to retrieve experiments for.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new experiment.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the experiment for.
* `profileId` - _required_ - View (Profile) ID to create the experiment for.
* `webPropertyId` - _required_ - Web property ID to create the experiment for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Delete an experiment.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the experiment belongs
* `experimentId` - _required_ - ID of the experiment to delete
* `profileId` - _required_ - View (Profile) ID to which the experiment belongs
* `webPropertyId` - _required_ - Web property ID to which the experiment belongs
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Returns an experiment to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve the experiment for.
* `experimentId` - _required_ - Experiment ID to retrieve the experiment for.
* `profileId` - _required_ - View (Profile) ID to retrieve the experiment for.
* `webPropertyId` - _required_ - Web property ID to retrieve the experiment for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Update an existing experiment. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID of the experiment to update.
* `experimentId` - _required_ - Experiment ID of the experiment to update.
* `profileId` - _required_ - View (Profile) ID of the experiment to update.
* `webPropertyId` - _required_ - Web property ID of the experiment to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Update an existing experiment.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID of the experiment to update.
* `experimentId` - _required_ - Experiment ID of the experiment to update.
* `profileId` - _required_ - View (Profile) ID of the experiment to update.
* `webPropertyId` - _required_ - Web property ID of the experiment to update.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists goals to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve goals for. Can either be a specific account ID or '~all', which refers to all the accounts that user has access to.
* `max-results` - _optional_ - The maximum number of goals to include in this response.
* `profileId` - _required_ - View (Profile) ID to retrieve goals for. Can either be a specific view (profile) ID or '~all', which refers to all the views (profiles) that user has access to.
* `start-index` - _optional_ - An index of the first goal to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID to retrieve goals for. Can either be a specific web property ID or '~all', which refers to all the web properties that user has access to.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new goal.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the goal for.
* `profileId` - _required_ - View (Profile) ID to create the goal for.
* `webPropertyId` - _required_ - Web property ID to create the goal for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Gets a goal to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve the goal for.
* `goalId` - _required_ - Goal ID to retrieve the goal for.
* `profileId` - _required_ - View (Profile) ID to retrieve the goal for.
* `webPropertyId` - _required_ - Web property ID to retrieve the goal for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing goal. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to update the goal.
* `goalId` - _required_ - Index of the goal to be updated.
* `profileId` - _required_ - View (Profile) ID to update the goal.
* `webPropertyId` - _required_ - Web property ID to update the goal.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing goal.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to update the goal.
* `goalId` - _required_ - Index of the goal to be updated.
* `profileId` - _required_ - View (Profile) ID to update the goal.
* `webPropertyId` - _required_ - Web property ID to update the goal.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists all profile filter links for a profile.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve profile filter links for.
* `max-results` - _optional_ - The maximum number of profile filter links to include in this response.
* `profileId` - _required_ - Profile ID to retrieve filter links for. Can either be a specific profile ID or '~all', which refers to all the profiles that user has access to.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property Id for profile filter links for. Can either be a specific web property ID or '~all', which refers to all the web properties that user has access to.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new profile filter link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create profile filter link for.
* `profileId` - _required_ - Profile ID to create filter link for.
* `webPropertyId` - _required_ - Web property Id to create profile filter link for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Delete a profile filter link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the profile filter link belongs.
* `linkId` - _required_ - ID of the profile filter link to delete.
* `profileId` - _required_ - Profile ID to which the filter link belongs.
* `webPropertyId` - _required_ - Web property Id to which the profile filter link belongs.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Returns a single profile filter link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve profile filter link for.
* `linkId` - _required_ - ID of the profile filter link.
* `profileId` - _required_ - Profile ID to retrieve filter link for.
* `webPropertyId` - _required_ - Web property Id to retrieve profile filter link for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Update an existing profile filter link. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which profile filter link belongs.
* `linkId` - _required_ - ID of the profile filter link to be updated.
* `profileId` - _required_ - Profile ID to which filter link belongs
* `webPropertyId` - _required_ - Web property Id to which profile filter link belongs
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Update an existing profile filter link.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which profile filter link belongs.
* `linkId` - _required_ - ID of the profile filter link to be updated.
* `profileId` - _required_ - Profile ID to which filter link belongs
* `webPropertyId` - _required_ - Web property Id to which profile filter link belongs
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists unsampled reports to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve unsampled reports for. Must be a specific account ID, ~all is not supported.
* `max-results` - _optional_ - The maximum number of unsampled reports to include in this response.
* `profileId` - _required_ - View (Profile) ID to retrieve unsampled reports for. Must be a specific view (profile) ID, ~all is not supported.
* `start-index` - _optional_ - An index of the first unsampled report to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `webPropertyId` - _required_ - Web property ID to retrieve unsampled reports for. Must be a specific web property ID, ~all is not supported.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Create a new unsampled report.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to create the unsampled report for.
* `profileId` - _required_ - View (Profile) ID to create the unsampled report for.
* `webPropertyId` - _required_ - Web property ID to create the unsampled report for.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Deletes an unsampled report.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to delete the unsampled report for.
* `profileId` - _required_ - View (Profile) ID to delete the unsampled report for.
* `unsampledReportId` - _required_ - ID of the unsampled report to be deleted.
* `webPropertyId` - _required_ - Web property ID to delete the unsampled reports for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Returns a single unsampled report.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to retrieve unsampled report for.
* `profileId` - _required_ - View (Profile) ID to retrieve unsampled report for.
* `unsampledReportId` - _required_ - ID of the unsampled report to retrieve.
* `webPropertyId` - _required_ - Web property ID to retrieve unsampled reports for.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists remarketing audiences to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - The account ID of the remarketing audiences to retrieve.
* `max-results` - _optional_ - The maximum number of remarketing audiences to include in this response.
* `start-index` - _optional_ - An index of the first entity to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `type` - _optional_
* `webPropertyId` - _required_ - The web property ID of the remarketing audiences to retrieve.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Creates a new remarketing audience.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - The account ID for which to create the remarketing audience.
* `webPropertyId` - _required_ - Web property ID for which to create the remarketing audience.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Delete a remarketing audience.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - Account ID to which the remarketing audience belongs.
* `remarketingAudienceId` - _required_ - The ID of the remarketing audience to delete.
* `webPropertyId` - _required_ - Web property ID to which the remarketing audience belongs.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Gets a remarketing audience to which the user has access.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - The account ID of the remarketing audience to retrieve.
* `remarketingAudienceId` - _required_ - The ID of the remarketing audience to retrieve.
* `webPropertyId` - _required_ - The web property ID of the remarketing audience to retrieve.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing remarketing audience. This method supports patch semantics.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - The account ID of the remarketing audience to update.
* `remarketingAudienceId` - _required_ - The ID of the remarketing audience to update.
* `webPropertyId` - _required_ - The web property ID of the remarketing audience to update.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Updates an existing remarketing audience.

*Tags:* `management`

#### Input Parameters
* `accountId` - _required_ - The account ID of the remarketing audience to update.
* `remarketingAudienceId` - _required_ - The ID of the remarketing audience to update.
* `webPropertyId` - _required_ - The web property ID of the remarketing audience to update.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Hashes the given Client ID.

*Tags:* `management`

#### Input Parameters
* `alt` - _optional_ - Data format for the response.
    Possible values: json.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists segments to which the user has access.

*Tags:* `management`

#### Input Parameters
* `max-results` - _optional_ - The maximum number of segments to include in this response.
* `start-index` - _optional_ - An index of the first segment to retrieve. Use this parameter as a pagination mechanism along with the max-results parameter.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Lists all columns for a report type

*Tags:* `metadata`

#### Input Parameters
* `reportType` - _required_ - Report type. Allowed Values: 'ga'. Where 'ga' corresponds to the Core Reporting API
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Creates an account ticket.

*Tags:* `provisioning`

#### Input Parameters
* `alt` - _optional_ - Data format for the response.
    Possible values: json.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Provision account.

*Tags:* `provisioning`

#### Input Parameters
* `alt` - _optional_ - Data format for the response.
    Possible values: json.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

### Insert or update a user deletion requests.

*Tags:* `userDeletion`

#### Input Parameters
* `alt` - _optional_ - Data format for the response.
    Possible values: json.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - An opaque string that represents a user for quota purposes. Must not exceed 40 characters.
* `userIp` - _optional_ - Deprecated. Please use quotaUser instead.

## License

**flow**ground :- Telekom iPaaS / googleapis-com-analytics-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
