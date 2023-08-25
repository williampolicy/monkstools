# monkstools
monkstools for team

begin to work. by Xiaowen kang. 2023.8.24.
check . well done.  by xiaowen kang. 2023.8.24
prepare for pypi package. by xiaowen kang. 2023.8.24.


### README.md

---

# monkstools: Advertising Delivery ROI Analysis Framework

`monkstools` is a Python module designed to analyze and visualize the Return on Investment (ROI) of product advertising across different platforms. It provides insights into which platform might yield the highest returns for advertising a particular product. While this framework is provided for demonstration purposes, the actual results in a production setting would be based on in-depth model training and real-world data.

## Overview

The primary goal of `monkstools` is to serve as a platform for programmers and data analysts to discuss, share, and collaborate on analyzing the ROI of advertising delivery. It's a template to kick-start discussions and exchange ideas on the intricacies of advertising dynamics across different platforms for various products.

## Key Components

**1. ProductPreference Class**
- **Purpose**: Retrieve product preference values for specified products and customer types.
- **Primary Method**: `get_preference(product_name, customer_type, verbose=False)`

**2. TransmissionCost Class**
- **Purpose**: Fetch transmission cost values for designated platforms and customer types.
- **Primary Method**: `get_cost(platform_name, customer_type, verbose=False)`

**3. ROICalculator Class**
- **Purpose**: Compute and visualize ROIs.
- **Primary Methods**:
  - `calculate(product_name, platform_name, verbose=False)`: Computes the ROI for a given product and platform.
  - `display_roi_matrix(roi_calculator, products, platforms)`: Visualizes the ROI matrix.

## Usage Guide

**1. Initialization**

   First, you need to initialize the `ROICalculator` object, which, in turn, initializes the `ProductPreference` and `TransmissionCost` objects.
   
   ```python
   preference_file = 'path_to_preference_file.csv'
   cost_file = 'path_to_cost_file.csv'
   roi_calculator = ROICalculator(preference_file, cost_file)
   ```

**2. Setting Up Products and Platforms**

   Define the list of products and platforms you're interested in analyzing.

   ```python
   products = ['Example Product 1', ...]  
   platforms = ['Example Platform 1', ...] 
   ```

**3. Displaying the ROI Matrix**

   Use the `display_roi_matrix` method of the `ROICalculator` class to compute and showcase the ROI matrix.

   ```python
   ROICalculator.display_roi_matrix(roi_calculator, products, platforms)
   ```

**4. Debugging and Logging**

   Set `verbose=True` when calling methods to print additional debugging and logging information.

## Note

This framework is intended for team discussions and sharing. The specific functions and data here are examples, and in a real-world scenario, deeper model training would be necessary. The final outcome is contingent on actual data and post-deep-training results. This is merely a conceptual framework and thought process to facilitate programmers' exchange of ideas.

--

To leverage this library, ensure `monkstools` is installed and data provided matches expected formats.

---

xiaowen kang. 2023.8.23


----
--

# monkstools: Advertising Delivery ROI Analysis Framework - Version V.0.10

## Introduction

`monkstools` is a versatile Python module tailored for analyzing and visualizing the Return on Investment (ROI) of product advertising across various platforms. This document offers a comprehensive guide on using the framework, based on version V.0.9, which has been refined through numerous iterations.

## Installation

Before diving into the framework's functionalities, it's essential to ensure `monkstools` is correctly installed:

```
pip install monkstools==0.10
```

Ensure you have the specified version V.0.9 for compatibility with the following usage instructions.

## Usage Example: `user_test_roi.py`

In the `user_test_roi.py` script, the focus is on showcasing the `monkstools` capabilities in deriving an ROI matrix, leveraging the intrinsic power of the library.

**Breakdown of the Example Script**:

1. **Dependencies**:
   - Essential modules and functions are imported at the outset. The `display_roi_matrix` function from the `monkstools.roi_calculator` module is crucial for our analysis.

2. **Function `test_display_roi_matrix`**:
   - **Data Source**: The paths for the preference and cost data files are dynamically located using `pkg_resources`. This method ensures a seamless fetch, irrespective of where the package is installed.
   - **ROI Calculator Initialization**: An instance of the `ROICalculator` class is created using the data files.
   - **Products & Platforms**: Lists of products and platforms define the scope of our analysis.
   - **Matrix Display**: The `display_roi_matrix` function visualizes the ROI matrix. To verify its accuracy, inspect the displayed chart or the saved "ROI_Comparison.png".

3. **Execution**: When the script is run directly, the ROI matrix visualization will be showcased, followed by a confirmation message.

## Using `monkstools` Library Professionally

1. **Initialization**: After installing `monkstools`, initialize the necessary components:
   ```python
   from monkstools.roi_calculator import ROICalculator, display_roi_matrix
   ```

2. **Data Integration**: Ensure your data files are structured appropriately. If you're using custom data, modify the columns in your CSV files to match the expected schema.

3. **Advanced Customization**: `monkstools` version V.0.9 also supports features like secondary preferences (`SecondaryPreference`). Make sure you explore and utilize these additional functionalities for in-depth analysis.

4. **Debugging**: The library incorporates verbose mode for enhanced debugging and insights. For instance:
   ```python
   preference = self.product_pref.get_preference(product_name, customer_type, verbose=True)
   ```

5. **Visualization**: The library boasts a rich visualization suite. Use the `display_roi_matrix` function for a holistic view, but do also delve into individual plotting options.

6. **Stay Updated**: While V.0.9 is the latest at this time, always check for newer versions. Features and functionalities may have been added or refined.

## Final Notes

Remember, the essence of `monkstools` lies in its adaptability. While it provides a robust framework, the true power emerges when it's tailored to specific datasets and advertising strategies. Use it as a stepping stone, and build upon its foundation for your unique advertising ROI analysis needs.

---
xiaowen kang 2023.8.23.

