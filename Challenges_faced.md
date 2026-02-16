⚠️ Challenges Faced During ETL Implementation

1️⃣ SSL Certificate Issues with Kaggle API

While attempting to fetch data programmatically using the Kaggle API, I encountered persistent SSL certificate verification errors.

**Root Cause:**

Corporate firewall restrictions were blocking secure API communication.

The Kaggle API token could not be validated due to SSL certificate verification failure.

Git installation settings and network security policies further restricted HTTPS requests.

**Troubleshooting Attempts:**

Disabled SSL verification temporarily within Python.

Manually created and configured the kaggle.json file.

Set environment variables to bypass certificate checks.

Reinstalled/configured Git with alternative SSL settings.

Despite multiple attempts, the issue persisted due to enterprise-level network restrictions.

**Final Resolution:**

Downloaded the dataset manually from Kaggle.

Processed the data locally to continue the ETL workflow.

This ensured project continuity while working within corporate network constraints.

2️⃣ Connecting Python to SQL Server

Establishing a connection between Python and SQL Server involved multiple configuration challenges.

**Issues Faced:**

ODBC driver not detected (Data source name not found error).

Incorrect driver string format in SQLAlchemy connection.

Server instance naming and accessibility issues.

SSL-related connection errors during database authentication.

Login timeout and network-related connectivity errors.

**Resolution Steps:**

Installed the correct ODBC Driver for SQL Server.

Correctly formatted the SQLAlchemy connection string.

Verified server instance name in SSMS.

Used Windows Authentication for secure connection.

Tested connectivity using a simple SELECT 1 query.

After resolving these configuration and driver-related issues, the connection was successfully established and data was loaded into SQL Server.

💡 Key Learnings

Corporate firewalls can interfere with API-based data extraction.

SSL verification errors are often network-level issues, not code-level issues.

Proper driver configuration is critical when connecting Python to SQL Server.

Always validate database connectivity using a minimal test query before loading data.