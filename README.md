# AI-Azure-Cosmos-DB-Azure-Blob-Storage
AI Python Apps for Azure Cosmos DB, Azure Blob Storage, Azure Container Registry, and Azure Container Apps

# Prep Work:
1. Create an azure subscription, azure resource group, azure cosmos db, azure blob storage account.
2. Download Azure Storage Explorer and Azurite for ABS.
3. Download document db quick start.

# Video Playlist:
https://www.youtube.com/playlist?list=PLHgX2IExbFos07Jf1iT2gg94A2IArbmLC

# Startup
1. Download and inspect the Python Quick start app for Azure Cosmos DB:
![image](https://github.com/AaronCWacker/AI-Azure-Cosmos-DB-Azure-Blob-Storage/assets/30595158/19a3fe6b-b3b9-4920-9902-a29d9527d029)

# Azure Cosmos DB (ACDB) Data Explorer
1. Inspect Data Explorer.  Which Features Do you See?
![image](https://github.com/AaronCWacker/AI-Azure-Cosmos-DB-Azure-Blob-Storage/assets/30595158/d75830f7-3e7f-4c05-b74a-fc4e13ea71d7)
1. New Container
2. New Database
3. New SQL Query
4. Open Query
5. New Stored Procedure
6. New Item
7. Upload Item

# Azure Blob Storage (ABS) Storage Explorer
1. Inspect Storage Explorer.  Enumerate Features.
![image](https://github.com/AaronCWacker/AI-Azure-Cosmos-DB-Azure-Blob-Storage/assets/30595158/64fb6170-9b91-4fe4-9c3a-51a9ffb38a5a)
1. Storage Accounts
2. Blob Containers
3. File Shares
4. Queues
5. Tables
6. Emulator (Download Azurite for local ABS Development

# Prompts for Basic Streamlit UI Development Using Python and AI
Create a streamlit python app that uses Azure Cosmos DB (ACDB) and Azure Blob Storage (ABS) to connect to Azure and run queries and save and download file resources and data.  The UI should include the following sidebar buttons adding appropriate emojis.  Create two expanders with emojis on labels one to contain the ACDB UI Elements and one for the ABS UI Elements.  For ACDB use this list of ffeatures to each create a button for:  1. New Container
2. New Database
3. New SQL Query
4. Open Query
5. New Stored Procedure
6. New Item
7. Upload Item  For ABS use this list of features to each create a button for:  1. Storage Accounts
2. Blob Containers
3. File Shares
4. Queues
5. Tables
6. Emulator (Download Azurite for local ABS Development  import the required python libraries for both Azure Cosmos DB and Azure Blob Storage.  Add basic UI to Supply a Connection String and Primary Key for ABS.  Do the Same to create basic UI connectivity to Azure Cosmos DB.  For both of those create the UI elements in center area with streamlit wide and keep the two expanders open by default on streamlit sidebar.

# Basic UI AI Generated Code (Enter and Test)

```
import streamlit as st
# Import Azure libraries (placeholder, you will need to replace with actual libraries)
# from azure.storage.blob import BlobServiceClient
# from azure.cosmos import CosmosClient

# Function to create ACDB buttons
def create_acdb_buttons():
    st.button("🗃️ New Container")
    st.button("💾 New Database")
    st.button("🔍 New SQL Query")
    st.button("📂 Open Query")
    st.button("📜 New Stored Procedure")
    st.button("➕ New Item")
    st.button("⬆️ Upload Item")

# Function to create ABS buttons
def create_abs_buttons():
    st.button("📦 Storage Accounts")
    st.button("🗂️ Blob Containers")
    st.button("📁 File Shares")
    st.button("🔗 Queues")
    st.button("📋 Tables")
    st.button("🧪 Emulator (Download Azurite)")

# UI for Azure Blob Storage connectivity
def abs_connectivity_ui():
    st.text_input("ABS Connection String", "Enter your connection string here")
    st.text_input("ABS Primary Key", "Enter your primary key here")

# UI for Azure Cosmos DB connectivity
def acdb_connectivity_ui():
    st.text_input("ACDB Connection String", "Enter your connection string here")
    st.text_input("ACDB Primary Key", "Enter your primary key here")

# Main app layout
def main():
    st.sidebar.title("Azure Integration App")

    # ACDB Expander
    with st.sidebar.expander("Azure Cosmos DB 🌐", expanded=True):
        create_acdb_buttons()

    # ABS Expander
    with st.sidebar.expander("Azure Blob Storage 🗄️", expanded=True):
        create_abs_buttons()

    # Main area for ABS and ACDB connectivity
    st.title("Azure Connectivity")
    with st.container():
        st.header("Azure Blob Storage Connectivity")
        abs_connectivity_ui()
        
        st.header("Azure Cosmos DB Connectivity")
        acdb_connectivity_ui()

if __name__ == "__main__":
    main()
```
