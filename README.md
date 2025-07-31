# AWS Cost Optimization: Finding and Removing Stale Resources
This AWS Lambda function automatically identifies and deletes stale EBS snapshots to help optimize AWS cloud storage costs.
### Key functionalities:
- Retrieves all EBS snapshots owned by the account.
- Fetches a list of currently running EC2 instances.
- Iterates through each snapshot to determine its relevance:
   - **Deletes snapshots** that are not associated with any EBS volume.
   - **Deletes snapshots** whose associated volumes no longer exist.
   - **Deletes snapshots** whose volumes are not attached to any running EC2 instance.



