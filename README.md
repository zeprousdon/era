soup = BeautifulSoup(html, 'html.parser')
filing_options = soup.find('div', attrs={'class': 'CaseDetails'}).find_all('input', {'checked': 'checked' })
filing_options_label_tag = [input_tag.find_next_sibling('label').text.strip() for input_tag in filing_options]
for label in filing_options_label_tag:
    print(label)
2023-SU-000141
01/19/2023
