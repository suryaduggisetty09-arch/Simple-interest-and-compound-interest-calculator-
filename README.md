P = float(input("Enter Principal Amount: "))
R = float(input("Enter Rate of Interest (% per year): "))

choice = input("Calculate for Years (Y) or Months (M): ").strip().upper()

if choice == "Y":
    T = float(input("Enter Time (Years): "))
elif choice == "M":
    months = float(input("Enter Time (Months): "))
    T = months / 12
else:
    print("Invalid choice!")
    exit()

# Simple Interest
SI = (P * R * T) / 100
Total_SI = P + SI

# Compound Interest
Amount_CI = P * (1 + R / 100) ** T
CI = Amount_CI - P

# Output
print("\n========== RESULT ==========")
print("Principal Amount :", P)
print("Rate of Interest :", R, "%")
print("Time             :", round(T, 2), "Years")

print("\nSimple Interest")
print("Interest         :", round(SI, 2))
print("Total Amount     :", round(Total_SI, 2))

print("\nCompound Interest")
print("Interest         :", round(CI, 2))
print("Total Amount     :", round(Amount_CI, 2))
