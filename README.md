# INTRODUCTION
In fact, data cleaning in Microsoft Excel offers a variety of methods. In my previous attempts, I highlighted the utilization of Excel functions to cleanse this identical dataset. 

However, today, I harnessed one of Excel's potent features to extract and transform the dataset, preparing it for subsequent analysis.

The messy dataset contains customer details that are jumbled together in a single cell within the spreadsheet. The information includes customer names, addresses, ages, and genders.

![THE dataset](https://github.com/dannieRope/Cleaning-Jumbled-Up-Customers-Details-in-Excel--APPROACH-1/assets/132214828/799790a7-6f7d-4f63-8577-a461298cd1f0)


The primary goal of this data cleaning exercise is to extract and organize the customer details into separate columns, ensuring that each piece of information, such as customer names, addresses, ages, and genders, occupies a designated column for a well-structured dataset.

# DATA CLEANING WITH POWER QUERY EDITOR

The process commences by importing the dataset into the Power Query Editor. To accomplish this, navigate to the Data tab,
select "Get Data," 
Click on "From File," and then opt for "From Excel Workbook."
Locate the dataset file at your chosen location.

![Screenshot (422)](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/45294ed7-d06c-45ae-ac91-cda8bc179548)

The Navigator window will appear. 

Select the worksheet that contains the data, and then click "Transform" at the bottom to import the data into Power Query Editor.

![datainpowerquery](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/f1f9165e-f526-411a-9a28-ecfe243377f6)

Now that we have the dataset in the power query editor, let's start by extracting the names of the customers from each row.

To start, let's eliminate the word 'name' that appears at the beginning of each row. This will provide a clean slate for extracting the customer names that follow the word 'Name'.

To accomplish this, navigate to the "Transform" tab in Power Query Editor. Then, select "Split Column" and opt for the "Delimiter" option. Specify the delimiter as 'Name' and click "OK."

![Screenshot (423)](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/160be028-ea17-46f3-b606-f61cd5d5b2d7)


![Screenshot (424)](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/2115ba77-8d39-4639-9ea1-0f350412f4bc)


You can remove the "1.1" column, as it contains empty rows. Afterward, split the column once more, but this time, specify 'address' as the delimiter.

This action will extract the names of the customers that appear before the word 'address'.

![Screenshot (425)](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/eec40c32-318d-4147-8a4f-8d652f30d714)

Let's proceed with renaming the column that contains the names as "FullName." Then, for the next step, extract the addresses of each customer.

![extract names](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/97dc8b54-8ea1-4424-8ad1-ac34ed1093e7)

To achieve this, split "Column1.2.2" once again, but this time specify "Age" as the delimiter. 

This action will extract the addresses that precede the word "Age" for each customer. Rename the column that contains the addresses as "Address". 

![address](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/4e85a3cf-3cc7-4fc0-840e-a3af54720311)

Next, let's proceed to extract the age of the customers.

To achieve this, split 'Column1.2.2.2' once more, but this time, specify "Gender" as the delimiter. 

This action will extract the numbers that appear before the word "gender" for each customer. Those numbers represent the ages of the customers. Finally, rename the column that contains the numbers as 'Age'.

Now, rename the last column, which contains the gender of the customers, as 'Gender'.

![Clean](https://github.com/dannieRope/Clening_Jumbled_Up_Customer_Details_In_Excel-Approach_3/assets/132214828/8adef375-bc0f-4947-a5cb-162daa1f3a97)

Great job! You've successfully transformed the dataset into a clean format, with all customer details, including name, address, age, and gender, separated into distinct columns.

