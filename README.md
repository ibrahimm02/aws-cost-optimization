# Optimizing AWS Cloud Costs - Detect Unused Resources

## Overview

A Lambda function that identifies and removes EBS snapshots that are no longer associated with any active EC2 instance which helps mitigate storage costs in the AWS environment.

The Lambda function fetches all EBS snapshots owned by the account and generates a list of active EC2 instances, including both running and stopped instances. For each snapshot, the function verifies if the associated volume, if it exists, is detached from any active instance. If a snapshot is found to be, it deletes, thereby optimizing storage costs.

