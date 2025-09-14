# Save test results to XRay

This section explains how to configure and use XRay integration to save test results from Lynqa executions.

## Overview

XRay integration allows you to automatically save test execution results from Lynqa to your XRay project, enabling better test management, reporting, and traceability.

## Prerequisites

Before setting up XRay integration, ensure you have:
- [ ] XRay project access and credentials
- [ ] Appropriate permissions in XRay
- [ ] Test cases mapped to XRay test issues
- [ ] Execution environment configured

## XRay Configuration

### Step 1: XRay Credentials

1. **Get XRay Credentials**
   - Log in to your XRay instance
   - Navigate to **Settings** > **API Keys**
   - Generate a new API key for Lynqa integration
   - Copy the API key and client ID

2. **Configure in Lynqa**
   - Go to **Settings** > **Integrations** > **XRay**
   - Enter your XRay server URL
   - Enter your client ID and API key
   - Test the connection

### Step 2: Project Mapping

1. **Select XRay Project**
   - Choose the target XRay project
   - Verify project permissions
   - Set as default project (optional)

2. **Configure Test Mapping**
   - Map Lynqa test cases to XRay test issues
   - Set up automatic mapping rules
   - Configure test case naming conventions

## Execution Configuration

### Automatic Result Saving

#### Enable Auto-Save
1. Go to **Execution Settings**
2. Enable **"Auto-save to XRay"**
3. Configure save triggers:
   - On execution completion
   - On test case completion
   - On execution failure
   - On manual trigger

#### Result Mapping
- **Test Results**: Map test outcomes to XRay statuses
- **Execution Details**: Include execution metadata
- **Screenshots**: Attach screenshots to test results
- **Logs**: Include execution logs
- **Custom Fields**: Map custom data fields

### Manual Result Saving

#### Save Individual Results
1. Navigate to **Execution Results**
2. Select the execution to save
3. Click **"Save to XRay"**
4. Review and confirm the mapping
5. Submit to XRay

#### Bulk Save Results
1. Go to **Execution History**
2. Select multiple executions
3. Choose **"Bulk Save to XRay"**
4. Configure batch settings
5. Process all selected executions

## Result Format and Mapping

### Test Execution Results

#### Execution Summary
- **Execution ID**: Unique Lynqa execution identifier
- **Start Time**: Execution start timestamp
- **End Time**: Execution end timestamp
- **Duration**: Total execution time
- **Status**: Overall execution status
- **Environment**: Target environment information

#### Test Case Results
- **Test Case ID**: Lynqa test case identifier
- **XRay Test Issue**: Mapped XRay test issue key
- **Status**: Test result status (PASS, FAIL, SKIP, etc.)
- **Duration**: Individual test execution time
- **Error Details**: Failure information and stack traces
- **Screenshots**: Attached screenshots and videos

### Custom Field Mapping

#### Standard Fields
- **Test Environment**: Environment where tests were executed
- **Browser/Platform**: Browser or platform information
- **Test Data**: Test data set used
- **Execution Notes**: Additional execution notes

#### Custom Fields
- **Priority**: Test priority level
- **Component**: Application component tested
- **Version**: Application version tested
- **Build Number**: Build or release number

## Advanced Configuration

### Result Filtering

#### Include/Exclude Rules
- **Test Status**: Include only specific test statuses
- **Test Categories**: Filter by test categories
- **Execution Types**: Include specific execution types
- **Date Ranges**: Filter by execution dates

#### Data Transformation
- **Status Mapping**: Custom status mapping rules
- **Field Transformation**: Transform data before saving
- **Data Validation**: Validate data before submission
- **Error Handling**: Configure error handling rules

### Notification Settings

#### Success Notifications
- **Email Alerts**: Notify on successful saves
- **Slack Notifications**: Post to Slack channels
- **Webhook Calls**: Send data to external systems

#### Error Notifications
- **Save Failures**: Alert on save failures
- **Mapping Errors**: Notify on mapping issues
- **Connection Errors**: Alert on XRay connection issues

## Monitoring and Troubleshooting

### Save Status Monitoring

#### Dashboard View
- **Recent Saves**: List of recent save operations
- **Save Statistics**: Success/failure rates
- **Error Logs**: Detailed error information
- **Performance Metrics**: Save operation performance

#### Status Indicators
- **Success**: Green indicator for successful saves
- **Warning**: Yellow indicator for warnings
- **Error**: Red indicator for failed saves
- **Pending**: Blue indicator for pending operations

### Common Issues

#### Connection Issues
- **Invalid Credentials**: Verify XRay credentials
- **Network Problems**: Check network connectivity
- **Server Unavailable**: Verify XRay server status
- **Permission Denied**: Check XRay permissions

#### Mapping Issues
- **Missing Test Issues**: Verify test case mapping
- **Invalid Field Values**: Check field value formats
- **Data Validation Errors**: Review data validation rules
- **Custom Field Issues**: Verify custom field configuration

#### Data Issues
- **Large Attachments**: Optimize screenshot/video sizes
- **Timeout Errors**: Increase timeout settings
- **Memory Issues**: Optimize data processing
- **Format Errors**: Verify data format compliance

## Best Practices

### Configuration
- [ ] Use descriptive execution names
- [ ] Set appropriate timeout values
- [ ] Configure proper error handling
- [ ] Test integration before production use

### Data Management
- [ ] Regularly clean up old execution data
- [ ] Optimize attachment sizes
- [ ] Use appropriate data retention policies
- [ ] Monitor storage usage

### Monitoring
- [ ] Set up monitoring alerts
- [ ] Regularly check save status
- [ ] Review error logs
- [ ] Monitor performance metrics

## API Integration

### REST API
- **Save Results**: Programmatically save results
- **Query Status**: Check save operation status
- **Retrieve Results**: Get saved result information
- **Update Results**: Modify saved results

### Webhook Integration
- **Execution Events**: Receive execution event notifications
- **Save Events**: Get save operation notifications
- **Error Events**: Receive error notifications
- **Status Updates**: Get real-time status updates

## Next Steps

- [Getting Started](getting-started.md) - Return to getting started guide
- [Launch Execution](launch-execution.md) - Learn how to launch executions
- [Control Execution](control-execution.md) - Learn how to control executions
