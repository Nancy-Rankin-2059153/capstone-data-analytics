# capstone-data-analytics
Final Capstone Project for Data Analytics Course

Arizona Energy Burden Analysis (Capstone Project)

Overview

	This project analyzes energy burden across Arizona counties over time, focusing on how energy costs relate to household income and how these relationships have changed across multiple years.

	Energy burden is defined as the percentage of household income spent on energy costs. This project integrates data from multiple sources to explore trends, identify disparities, and evaluate the factors that drive variation across counties.

	The analysis is supported by data preprocessing, regression modeling, and an interactive Power BI dashboard designed for non-technical stakeholders.

Objectives

	Analyze how median income has changed across Arizona counties (2010–2024)
	
	Compare energy costs relative to income over time
	
	Measure variation in energy burden across counties
	
	Identify key factors influencing energy burden using regression models
	
	Communicate findings through an accessible Power BI dashboard
	
Project Structure

/data

    raw/                # Original datasets (Census, EIA, etc.)
	
    processed/          # Cleaned and standardized datasets used in modeling
	

/notebooks

    data_cleaning/      # Year-specific preprocessing notebooks
	
    feature_engineering/
	
    modeling/

/powerbi

    Energy_Burden_Report.pbix

/output

    figures/            # Exported visuals used in report
	
    regression_results/

/docs

    capstone_report/    # Final APA report (Chapters 1–5)
	
    instructional_guide/
	
Data Sources

	This project uses publicly available datasets, including:

		U.S. Census Bureau (ACS) – Median income and housing characteristics
		
		U.S. Energy Information Administration (EIA) – Electricity revenue, sales, and customer counts
		
		Supplemental datasets for inflation and economic context

	Note: Raw datasets were transformed and standardized prior to use. Some files in /processed are derived datasets created during this project.

Data Processing

	Data preparation was a critical component of this project and included:

		Cleaning inconsistent column naming (e.g., verbose Census labels)
		
		Removing margin-of-error and percentage distribution fields
		
		Converting wide-format datasets into usable structured formats
		
		Standardizing county-level aggregation
		
		Creating comparable structures across years (2010, 2015, 2018, 2020, 2024)

	Each year was processed separately to account for schema differences, then aligned for modeling and visualization.

Modeling Approach

	Linear regression models were developed to evaluate the relationship between:

		Median income
		
		Energy cost (price per kilowatt-hour)
		
		Energy usage

	Two modeling periods were used due to differences in data structure:

		2010–2015 Model
		
		2018–2024 Model

	Outputs include:

		Model coefficients
		
		R² values (variance explained)
		
		Actual vs. predicted energy burden comparisons
		
		Power BI Dashboard

The Power BI report (/powerbi/Energy_Burden_Report.pbix) presents:

	Energy burden trends over time
	
	County-level comparisons
	
	Income vs. energy burden relationships
	
	Year-over-year changes
	
	Regression results and model interpretation

    Key Features
	
		Interactive slicers (county, year)
		
		Multi-page layout optimized for desktop and mobile
		
		Regression results visualization
		
		Accessibility considerations (alt text, readable layouts)

	Manually Entered Tables (Power BI)
	
	The Power BI model includes internally stored tables used to support regression reporting:
	
		Model Period – Reference table used for filtering model views
		
		R² Score – Stores model performance values
		
		Regression Results – Stores coefficients and regression outputs
		
	These tables are manually maintained and do not refresh from external sources.
	
How to Use This Repository

	Run the Analysis
	
	Open notebooks in /notebooks
	
	Ensure required Python libraries are installed (pandas, scikit-learn, etc.)
	
	Run preprocessing and modeling steps
	
View the Dashboard

	Open the .pbix file in Power BI Desktop
	
	Click Refresh to reload data (if needed)
	
	Interact with slicers and report pages
	
Key Insights (Summary)

	Energy burden varies significantly across Arizona counties
	
	Income and energy costs both contribute to variation, but not equally across time periods
	
	Structural differences between earlier and later datasets required separate modeling approaches
	
	Regression models explain a meaningful portion of variation, but not all—indicating additional external factors
	
Technologies Used
	Python (pandas, scikit-learn)
	
	Power BI
	
	Excel / CSV data processing
	
	Jupyter / Google Colab
	
Limitations

	Differences in data structure across years required segmented modeling
	
	Some datasets required manual transformation and interpretation
	
	Utility-to-county relationships were approximated based on available data
	
Author

	Nancy Rankin
	
	Data Analytics & Computer Programming (B.S.) – May 2026
	
License

	This project is for academic and portfolio purposes. Data sources remain the property of their respective providers.
