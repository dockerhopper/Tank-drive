package frc.robot;

import edu.wpi.first.wpilibj.Joystick;
import edu.wpi.first.wpilibj.TimedRobot;
import edu.wpi.first.wpilibj.drive.DifferentialDrive;
//import edu.wpi.first.wpilibj.motorcontrol.MotorController;
import edu.wpi.first.wpilibj.motorcontrol.MotorControllerGroup;
import com.ctre.phoenix.motorcontrol.can.WPI_VictorSPX;
//import com.ctre.phoenix.motorcontrol.VictorSPXSimCollection;
//import edu.wpi.first.wpilibj.XboxController;

public class Robot extends TimedRobot {
  DifferentialDrive m_myRobot;
  Joystick _joystick = new Joystick(0);

  //MotorController m_leftMotor = new PWMSparkMax(0);
  //MotorController m_rightMotor = new PWMSparkMax(1);

  //XboxController driverGamepad = new XboxController(0);

  WPI_VictorSPX m_frontLeft = new WPI_VictorSPX(1);
  // VictorSPXSimCollection m_frontLeftSim = m_frontLeft.getSimCollection();
  WPI_VictorSPX m_backLeft = new WPI_VictorSPX(2);
  //VictorSPXSimCollection m_backLeftSim = m_backLeft.getSimCollection();
  MotorControllerGroup m_left = new MotorControllerGroup(m_frontLeft, m_backLeft);

  WPI_VictorSPX m_frontRight = new WPI_VictorSPX(3);
  //VictorSPXSimCollection m_righRightSim = m_frontRight.getSimCollection();
  WPI_VictorSPX m_backRight = new WPI_VictorSPX(4);
  //VictorSPXSimCollection m_backRightSim = m_backRight.getSimCollection();
  MotorControllerGroup m_right = new MotorControllerGroup(m_frontRight, m_backRight);

  DifferentialDrive m_drive = new DifferentialDrive(m_left, m_right);
  

  @Override
  public void robotInit() {
    // We need to invert one side of the drivetrain so that positive voltages
    // result in both sides moving forward. Depending on how your robot's
    // gearbox is constructed, you might have to invert the left side instead.
    m_right.setInverted(true);

    //m_leftStick = new Joystick(0);
    //m_rightStick = new Joystick(1);
  }

  @Override
  public void teleopPeriodic() {
    m_drive.tankDrive(_joystick.getRawAxis(1), _joystick.getRawAxis(5));
  }
}
