# Experiment 1.A  Employee Data Display Using Python

## Aim

To collect employee details, validate inputs, and calculate gross and net salary using Python.

## Algorithm

1. **Start** the program.
2. **Read Employee Details** from the user:
   * Input `name` (String) for the employee's full name.
   * Input `emp_id` (String) for the employee's identification number.
   * Input `basic` (Float) for the employee's basic salary.
3. **Validate Input**:
   * Ensure `basic` is a valid numeric value and check if `basic < 0`. If invalid or negative, display an appropriate error message and terminate the program.
4. **Compute Allowances**:
   * Calculate House Rent Allowance: $\text{HRA} = 0.15 \times \text{basic}$.
   * Calculate Dearness Allowance: $\text{DA} = 0.10 \times \text{basic}$.
5. **Compute Gross Salary**:
   * Calculate total earnings before deductions: $\text{Gross Salary} = \text{basic} + \text{HRA} + \text{DA}$.
6. **Compute Tax Deduction**:
   * Calculate income tax at $8\%$ of gross pay: $\text{Tax} = 0.08 \times \text{Gross Salary}$.
7. **Compute Net Salary**:
   * Calculate take-home pay: $\text{Net Salary} = \text{Gross Salary} - \text{Tax}$.
8. **Display Formatted Payroll Report**:
   * Print a structured summary displaying `name`, `emp_id`, `basic`, `HRA`, `DA`, `Gross Salary`, `Tax`, and `Net Salary` formatted to two decimal places.
9. **Stop** the program.

## Program


## Output

    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    basic = float(input("Enter Basic Salary: "))

    if basic < 0:
        print("Error: Salary cannot be negative.")
    else:
        hra = 0.15 * basic
        da = 0.10 * basic

        gross = basic + hra + da

        tax = 0.08 * gross

        net = gross - tax

        print("\n------ EMPLOYEE PAYROLL REPORT ------")
        print("Employee Name :", name)
        print("Employee ID   :", emp_id)
        print("Basic Salary  : Rs.", format(basic, ".2f"))
        print("HRA           : Rs.", format(hra, ".2f"))
        print("DA            : Rs.", format(da, ".2f"))
        print("Gross Salary  : Rs.", format(gross, ".2f"))
        print("Tax           : Rs.", format(tax, ".2f"))
        print("Net Salary    : Rs.", format(net, ".2f"))

## ✅ Result
Enter Employee Name: Rakhav
Enter Employee ID: EMP101
Enter Basic Salary: 30000

------ EMPLOYEE PAYROLL REPORT ------
Employee Name : Rakhav
Employee ID   : EMP101
Basic Salary  : Rs. 30000.00
HRA           : Rs. 4500.00
DA            : Rs. 3000.00
Gross Salary  : Rs. 37500.00
Tax           : Rs. 3000.00
Net Salary    : Rs. 34500.00

The program successfully accepts and validates employee details, calculates allowances and deductions, and displays a well-formatted salary report.
