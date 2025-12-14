def kinetic_energy(mass, velocity):
    return 0.5 *mass * velocity ** 2

def potential_energy(mass, height, gravity=9.81):
    return mass * gravity *height

def electrical_energy(power, time):
    return power * time

def main():
    print("=== Energy Calculator ===")
    print("1. Kinetic Energy")
    print("2. Potential Energy")
    print("3. Electrical Energy")

    choice = input("Choose an option (1/2/3):")

    if choice == "1":
        mass = float(input("Enter mass (kg): "))
        velocity = float(input("Enter velocity (m/s): "))
        energy = kinetic_energy(mass, velocity)
        print(f"Kinetic Energy ={energy:.2f}joules")

    elif choice == "2":
        mass = float(input("Enter mass (kg): "))
        height =float(input("Enter height (m): "))
        energy = potential_energy(mass, height)
        print(f"Potential Energy ={energy:.2f} Joules")
    
    elif choice =="3":
        power = float(input("Enter power (Watts): "))
        time = float(input("Enter time (seconds): "))
        energy = electrical_energy(power, time)
        print(f"Electrical Energy ={energy:.2f} Joules")

    else:
        print("invalid choice!")

if __name__ == "__main__":
    main()
