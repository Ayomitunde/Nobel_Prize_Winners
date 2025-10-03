                                Nobel Prize Winners

                                **Data Cleaning
**Reading the dataset(it was sourced from OpenDataSoft's website)
**Checking the properties of each column(ie Column Name, Data Type , missing values %)
**for columns that are not in their proper data type, they were converted data types [Born , Died]
**Create new column [Age , AgeGetPrize] from simple arithemtic operation
** Create new column column status from citizen_status function
                def citizen_status(status):
                    if status['Born country'] != status['Organization country']:
                        return "Immigrant Laurates"
                    else:
                        return "Total Laurates"
            nobel_redo['status'] = nobel_redo.apply(citizen_status, axis = 1)
**Create new column 'Age_groups' from age_groups function
**Create new column 'Years_Decade' from Years_Decade function
**Dropping columns that are needed in the analysis : Born country code, Died country code, Overall motivation, Born Year, Died Year, Firstname, Surname
                                **Visualizations
**Display No of women and men that won the nobel laurates
**Display of country with most winners : USA has most winners
**What Category do these prizes belong to : Medicene & Physics are the categories with most winners
**There are more immigrant laurates  : 52.17% of winners are immigrants
**During the periods of WW1 and WW2, the numbers of winners dropped but rose gradually ever since the, there was small dip in the 1980s
**University of California provided the highest number of nobel laurates, followed closely by Harvard University
**Most winners won the nobel prize in their middle age