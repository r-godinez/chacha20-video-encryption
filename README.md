# ChaCha20 Video Encryption System

## Overview
This project implements a real-time video encryption system using the ChaCha20 stream cipher. The system captures video from a webcam on a Raspberry Pi, encrypts each frame using ChaCha20 encryption, and transmits the encrypted data over a network to a receiving computer for decryption and display.

## Project Purpose & Learning Objectives
This project demonstrates:
- **Real-time cryptographic operations** on video data
- **Stream cipher implementation** using ChaCha20
- **Network programming** with socket communication
- **Performance optimization** for real-time video processing
- **Cryptographic key management** and nonce generation
- **Cross-platform development** (Raspberry Pi to PC communication)

## Technical Implementation

### Architecture
- **Sender (Raspberry Pi)**: Captures video, encrypts frames, sends over network
- **Receiver (PC)**: Receives encrypted data, decrypts frames, displays video

### Key Features
- **ChaCha20 Stream Cipher**: Uses 32-byte key and 16-byte nonce per frame
- **Real-time Processing**: Optimized for live video streaming
- **Performance Monitoring**: Tracks encryption/transmission times and FPS
- **Frame-by-frame Encryption**: Each frame uses a unique nonce for security
- **Automatic File Management**: Saves encrypted frames and decrypted images

### Security Features
- **Unique Nonce per Frame**: Prevents replay attacks and ensures frame uniqueness
- **Secure Key Management**: 32-byte ChaCha20 key for strong encryption
- **Frame Integrity**: Maintains video quality while ensuring confidentiality

## File Structure
```
chacha20-video-encryption/
├── src/
│   ├── sender.py          # Raspberry Pi video capture and encryption
│   └── receiver.py        # PC video decryption and display
├── video_link.txt         # Demonstration video links
└── README.md             # This file
```

## Dependencies
- **Python 3.8+**
- Project Python packages are listed in `requirements.txt`:
  - `opencv-python` - Video capture and processing
  - `cryptography` - ChaCha20 encryption implementation
  - `numpy` - Array operations for image data

## Installation & Setup

### Prerequisites
Install dependencies using `requirements.txt` (recommended to use a virtual environment):
```bash
pip install -r requirements.txt
```

### Configuration
1. Update IP addresses in both `sender.py` and `receiver.py`
2. Ensure both devices are on the same network
3. Configure camera settings (resolution, frame rate) as needed

## Usage

### Running the System
1. **Start the receiver** (PC):
   ```bash
   python src/receiver.py
   ```

2. **Start the sender** (Raspberry Pi):
   ```bash
   python src/sender.py
   ```

### Controls
- **'q' key**: Quit the application
- **Frame limit**: Set to 100 frames by default (configurable)

## Performance Metrics
The system tracks and displays:
- **Encryption time** per frame
- **Transmission time** per frame
- **FPS (Frames Per Second)** calculation
- **Total processing time** for performance analysis

## Demonstration

### Video Demonstration
[![ChaCha20 Video Encryption Demo](https://img.youtube.com/vi/ZtI_uvnqqgs/0.jpg)](https://www.youtube.com/watch?v=ZtI_uvnqqgs)

**Click the image above to watch the full demonstration**

The video shows:
- Real-time video encryption and decryption
- Performance metrics and system operation
- Cross-platform communication between Raspberry Pi and PC
- Live encryption/transmission timing measurements

## Technical Specifications
- **Encryption Algorithm**: ChaCha20 stream cipher
- **Key Size**: 32 bytes (256 bits)
- **Nonce Size**: 16 bytes (128 bits)
- **Video Resolution**: 640x480 (configurable)
- **Network Protocol**: TCP socket communication
- **Port**: 8080 (configurable)

## Security Considerations
- **Forward Secrecy**: Each frame uses a unique nonce
- **Key Management**: Secure key distribution assumed
- **Network Security**: Implement additional TLS/SSL for production use
- **Nonce Generation**: Uses cryptographically secure random generation

## Future Enhancements
- **Key Exchange Protocol**: Implement secure key distribution
- **Compression**: Add video compression before encryption
- **Error Handling**: Improve network error recovery
- **GUI Interface**: Add user-friendly interface
- **Multi-client Support**: Support multiple receivers

## Educational Value
This project serves as an excellent learning tool for:
- Understanding stream ciphers and their applications
- Real-time cryptographic system design
- Network programming and socket communication
- Performance optimization in cryptographic applications
- Cross-platform development and deployment

## License
This project is part of ECE4301 coursework and is intended for educational purposes.


## Video Link
    https://www.youtube.com/watch?v=ZtI_uvnqqgs
         