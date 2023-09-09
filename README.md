# Detect Malicious URLs using Machine Learning

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kolo-vrat/detect-malicious-url-ml/blob/main/DetectMaliciousURL.ipynb)

This project is created as part for the course Digital Forensics.

#### Install the required packages

The required packages are located in the requirements.txt file. You can use this command to install them. 

```shell
python3 -m pip install -r requirements.txt
```

#### Goal

The goal of this project is to use Machine Learning models for detecting whether a URL is malicious or not. A dataset of 447502 records of URLs is used which is taken from [Kaggle](https://www.kaggle.com/datasets/siddharthkumar25/malicious-and-benign-urls).

#### Features

Using the dataset 20 lexical fetures were extracted from URLs. The classifiers used are: Decision Tree, Random Forest, Naive Bayes and Logistic Regression.

| Feature Name | Explanation |
| ------------ | ----------- |
| length | Length of the entire URL |
| primary_domain_length | Length of the primary domain |
| primary_domain_length_url_length_ratio | The ratio between the length of the primary domain and the length of the entire URL |
| path_length | Length of the path path |
| path_length_url_length_ratio | The ratio between the length of the path and the length of the entire URL |
| number_digits | Number of characters that are numbers |
| number_special_characters | Number of special characters: ':', '//', '.', ':', '/', '?=', ',', ';', '(',')',']','+' |
| number_special_characters_path | Number of special characters in the path |
| number_dots | Number of dots in the URL |
| number_subdomains | Number of subdomains |
| url_scheme | Address protocol or scheme, whether https or http |
| host_is_ip | Is the host part an IP address or a character string |
| host_has_port | Does the host have a port specified |
| digit_letter_ratio | Ratio between the number of digits and letters |
| number_path_subdirectories | Number of subdirectories in the path |
| number_single_character_directories | Number of subdirectories that are single character only |
| number_queries | Number of query parameters |
| is_encoded | Are there any characters that are encoded, such as %20 which indicates a space character |
| number_encoded_char | Number of encoded characters |
| url_entropy | URL entropy |

#### Conclusion

The results obtained are good, however, host-based features are not used such as DNS records, domain creation date, nor are features based on the content the URL points to. Such features will introduce a time delay. Using only lexical features can give fast results because they can be calculated quickly.
