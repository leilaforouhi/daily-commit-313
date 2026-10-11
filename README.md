def format_duration(total_seconds):
    if total_seconds < 0:
        raise ValueError("Duration cannot be negative")

    hours, remainder = divmod(total_seconds, 3600)
    minutes, seconds = divmod(remainder, 60)

    return f"{hours:02}:{minutes:02}:{seconds:02}"


if __name__ == "__main__":
    durations = [45, 125, 3661, 7325]

    for duration in durations:
        print(f"{duration} seconds -> {format_duration(duration)}")
