# blood-pressureclass BloodPressureMonitor:
    def __init__(self):
        # Initialize connection to the monitor
        pass

    def read_data(self):
        # Mock function to simulate reading from a blood pressure monitor
        # In a real scenario, this would communicate with the hardware
        return 120, 80  # Systolic, Diastolic mock values

    def process_data(self, systolic, diastolic):
        # Process raw data here (if necessary)
        return systolic, diastolic

    def display_data(self, systolic, diastolic):
        # Display or store the processed data
        print(f"Systolic: {systolic} mmHg, Diastolic: {diastolic} mmHg")

def main():
    bp_monitor = BloodPressureMonitor()
    raw_systolic, raw_diastolic = bp_monitor.read_data()
    systolic, diastolic = bp_monitor.process_data(raw_systolic, raw_diastolic)
    bp_monitor.display_data(systolic, diastolic)

if __name__ == "__main__":
    main()
