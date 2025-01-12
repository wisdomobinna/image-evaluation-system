# Image-evaluator (Image Evaluation Distribution System (IEDS)
A React-based application that systematically distributes AI-generated images to evaluators via Qualtrics. Manages evaluation of 300 artworks (125 AI-only, 175 AI-collaborative) across 250 evaluators, ensuring each piece receives ~12.5 evaluations. Features Firebase integration for image storage and evaluation tracking.

## Features

- Balanced distribution of AI-only and AI-collaborative images
- Real-time evaluation tracking via Firebase
- Seamless Qualtrics integration
- Automatic image randomization
- Progress monitoring and completion tracking

## Prerequisites

- Node.js (v14 or higher)
- Firebase account
- Qualtrics account
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/image-evaluation-system.git
cd image-evaluation-system
```

2. Install dependencies:
```bash
npm install
```

3. Configure Firebase:
- Create a Firebase project
- Enable Storage and Firestore
- Create two folders in Storage: `ai-only` and `ai-involved`
- Copy your Firebase config to `src/firebase.js`

4. Set up environment variables:
```bash
cp .env.example .env
```
Edit `.env` with your configuration details.

## Project Structure

```
src/
├── components/
│   └── ImageEvaluator.js
├── firebase.js
├── App.js
└── index.js
```

## Configuration

1. Firebase Storage Structure:
```
storage/
├── ai-only/       # 125 AI-generated images
└── ai-involved/   # 175 AI-collaborative images
```

2. Firestore Collections:
```
collections/
├── evaluation_stats/
├── evaluators/
└── assignments/
```

## Usage

1. Start development server:
```bash
npm start
```

2. Build for production:
```bash
npm run build
```

3. Deploy to Firebase:
```bash
firebase deploy
```

## Evaluation Process

- Each evaluator receives 12 images (6 AI-only, 6 AI-collaborative)
- Images are distributed to ensure ~12.5 evaluations per piece
- Progress is tracked in real-time
- Results are collected via Qualtrics

## Monitoring

Access evaluation progress through Firebase Console:
- Track completion rates
- Monitor evaluation distribution
- View individual evaluator progress

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/name`)
3. Commit changes (`git commit -am 'Add feature'`)
4. Push to branch (`git push origin feature/name`)
5. Open a Pull Request

## License

MIT License - see LICENSE.md

## Contact

Your Name - wko7@georgetown.edu
Project Link: https://github.com/wisdomobinna/image-evaluation-system
