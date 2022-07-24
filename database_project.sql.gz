-- phpMyAdmin SQL Dump
-- version 5.1.3
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Apr 15, 2022 at 07:40 PM
-- Server version: 10.4.24-MariaDB
-- PHP Version: 8.1.4

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `database project`
--

-- --------------------------------------------------------

--
-- Table structure for table `appointment`
--

CREATE TABLE `appointment` (
  `Appointment_id` varchar(10) NOT NULL,
  `Appointment_date` date NOT NULL,
  `Appointment_time` time NOT NULL,
  `Doctor_id` varchar(10) NOT NULL,
  `Patient_id` varchar(10) NOT NULL,
  `Patient_name` varchar(20) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `appointment`
--

INSERT INTO `appointment` (`Appointment_id`, `Appointment_date`, `Appointment_time`, `Doctor_id`, `Patient_id`, `Patient_name`) VALUES
('123001', '2022-04-12', '10:00:00', '2000', '121', 'Hanif'),
('123002', '2022-04-12', '12:00:00', '2003', '122', 'Plabon'),
('123003', '2022-04-13', '10:00:00', '2002', '123', 'Dutta'),
('123004', '2022-04-13', '12:00:00', '2000', '124', 'Ridoy'),
('123005', '2022-04-14', '10:00:00', '2005', '125', 'Lipu'),
('123006', '2022-04-14', '12:00:00', '2002', '126', 'Amit');

-- --------------------------------------------------------

--
-- Table structure for table `doctors`
--

CREATE TABLE `doctors` (
  `Doctor_id` varchar(10) NOT NULL,
  `Doctor_name` varchar(20) DEFAULT NULL,
  `Doctor_age` varchar(4) DEFAULT NULL,
  `Doctor_speciality` varchar(20) DEFAULT NULL,
  `Doctor_salary` varchar(10) DEFAULT NULL,
  `Hospital_id` varchar(10) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `doctors`
--

INSERT INTO `doctors` (`Doctor_id`, `Doctor_name`, `Doctor_age`, `Doctor_speciality`, `Doctor_salary`, `Hospital_id`) VALUES
('2000', 'Dr. Devi Shetty', '34', 'Heart', '80000', '10001'),
('2001', 'Dr. Nafiz', '39', 'Kidney', '25000', '10002'),
('2002', 'Dr. Bidita', '26', 'Brain', '35000', '10003'),
('2003', 'Dr. Mahmud', '30', 'Liver', '40000', '10002'),
('2004', 'Dr. Rahman', '38', 'Skin', '45000', '10004'),
('2005', 'Dr. Diba', '40', 'Heart', '65000', '10003');

-- --------------------------------------------------------

--
-- Table structure for table `hospital`
--

CREATE TABLE `hospital` (
  `Hospital_id` varchar(10) NOT NULL,
  `Hospital_name` varchar(30) NOT NULL,
  `Hospital_address` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `hospital`
--

INSERT INTO `hospital` (`Hospital_id`, `Hospital_name`, `Hospital_address`) VALUES
('10001', 'United Hospital', 'Dhanmondi, Dhaka-1215'),
('10002', 'BRB Hospital', 'Gulshan, Dhaka-1213'),
('10003', 'Apollo Hospital', 'Baridhara, Dhaka-1211'),
('10004', 'Square Hospital', 'Panthopath, Dhaka-1216');

-- --------------------------------------------------------

--
-- Table structure for table `medicines`
--

CREATE TABLE `medicines` (
  `Medicine_id` varchar(10) NOT NULL,
  `Medicine_name` varchar(20) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `medicines`
--

INSERT INTO `medicines` (`Medicine_id`, `Medicine_name`) VALUES
('01', 'Napa'),
('02', 'Seclo'),
('03', 'Napa Rapid'),
('04', 'Fexo'),
('05', 'E_Cap');

-- --------------------------------------------------------

--
-- Table structure for table `nurses`
--

CREATE TABLE `nurses` (
  `Nurses_id` varchar(10) NOT NULL,
  `Nurses_name` varchar(20) DEFAULT NULL,
  `Nurses_age` varchar(4) DEFAULT NULL,
  `Nurses_salary` varchar(10) DEFAULT NULL,
  `Doctor_id` varchar(10) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `nurses`
--

INSERT INTO `nurses` (`Nurses_id`, `Nurses_name`, `Nurses_age`, `Nurses_salary`, `Doctor_id`) VALUES
('1011', 'Rina', '23', '25000', '2005'),
('1012', 'Nipa', '25', '22000', '2001'),
('1013', 'Riya', '22', '22000', '2004'),
('1014', 'Nila', '33', '25000', '2003'),
('1015', 'Popy', '43', '26000', '2000'),
('1016', 'Rima', '45', '23000', '2002'),
('1017', 'Mim', '36', '23000', '2003'),
('1018', 'Anny', '39', '25000', '2000');

-- --------------------------------------------------------

--
-- Table structure for table `patients`
--

CREATE TABLE `patients` (
  `Patient_id` varchar(10) NOT NULL,
  `Patient_name` varchar(20) DEFAULT NULL,
  `Medicine_name` varchar(20) DEFAULT NULL,
  `Room_num` varchar(20) DEFAULT NULL,
  `Doctor_id` int(11) NOT NULL,
  `Nurse_id` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `patients`
--

INSERT INTO `patients` (`Patient_id`, `Patient_name`, `Medicine_name`, `Room_num`, `Doctor_id`, `Nurse_id`) VALUES
('111', 'Apon', 'Napa', '201', 2005, 1011),
('112', 'Badshah', 'Fexo', '103', 2004, 1013),
('113', 'Alam', 'Seclo', '301', 2000, 1018),
('114', 'Mina', 'E-Cap', '202', 2002, 1016),
('115', 'Raju', 'Napa Rapid', '102', 2000, 1015),
('116', 'Arnob', 'Napa', '303', 2001, 1012),
('117', 'Turjo', 'Napa Rapid', '302', 2003, 1017),
('118', 'Fuad', 'Seclo', '101', 2003, 1014);

-- --------------------------------------------------------

--
-- Table structure for table `roomnum`
--

CREATE TABLE `roomnum` (
  `Room_num` varchar(20) NOT NULL,
  `Floor_num` varchar(20) DEFAULT NULL,
  `Room_type` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `roomnum`
--

INSERT INTO `roomnum` (`Room_num`, `Floor_num`, `Room_type`) VALUES
('101', '1', 'AC Cabin'),
('102', '1', 'Non-AC Cabin'),
('103', '1', 'Non-AC Cabin'),
('201', '2', 'Non-AC Cabin'),
('202', '2', 'AC Cabin'),
('203', '2', 'Non-AC Cabin'),
('301', '3', 'AC Cabin'),
('302', '3', 'AC Cabin'),
('401', '4', 'Non-AC Cabin'),
('402', '2', 'ICU');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `doctors`
--
ALTER TABLE `doctors`
  ADD PRIMARY KEY (`Doctor_id`);

--
-- Indexes for table `hospital`
--
ALTER TABLE `hospital`
  ADD PRIMARY KEY (`Hospital_id`);

--
-- Indexes for table `medicines`
--
ALTER TABLE `medicines`
  ADD PRIMARY KEY (`Medicine_id`);

--
-- Indexes for table `nurses`
--
ALTER TABLE `nurses`
  ADD PRIMARY KEY (`Nurses_id`);

--
-- Indexes for table `patients`
--
ALTER TABLE `patients`
  ADD PRIMARY KEY (`Patient_id`);

--
-- Indexes for table `roomnum`
--
ALTER TABLE `roomnum`
  ADD PRIMARY KEY (`Room_num`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
