# lab_13
#The homework of lab_13
# lab_13

class delivery_personnel:

	def __init__(self, name, years_of_services, company, is_drone, zip_codes_covered):
		self.name              = name
		self.years_of_services = years_of_services
		self.company           = company
		self.is_drone          = is_drone
		self.zip_codes_covered = zip_codes_covered

	# Getters
	def get_years_of_services(self):
		return(self.years_of_services)

	def get_company(self):
		return(self.company)

	def get_zip_codes_covered(self):
		return(self.zip_codes_covered)

	# Setters
	def set_years_of_services(self, y):
		self.years_of_services = y

	def set_company(self, c):
		self.compnay = c

	def set_zip_codes_covered(self, z):
		self.zip_codes_covered = z

	# Methods
	def deliver(self, zip_codes):
		while (zip_codes != None):
			if (zip_codes in self.zip_codes_covered):
				return(zip_codes)
				zip_codes += 1
			else:
				return("Not completed.")
		else:
			zip_codes == self.zip_codes_covered

def main():

	deliver_1 = delivery_personnel(name = "Jason", years_of_services = 4, company = "Amazon", is_drone = False, zip_codes_covered = [20016, 20017, 20018])

	print(deliver_1.deliver(zip_codes = 20016))

if __name__ == '__main__':
	main()

